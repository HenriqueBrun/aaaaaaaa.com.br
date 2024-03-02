<script setup>
import { useDebounceFn } from '@vueuse/core'
import { ref, computed } from 'vue'
import router from '../router'

const treatedRoutes = getRoutes();
const AAAAAAAA = 'AAAAAAAA'

const onInput = useDebounceFn(() => {
  if (treatedRoutes.findIndex(element => element.includes(model.value.toLowerCase())) < 0 || !model.value.includes(AAAAAAAA)) {
    model.value = AAAAAAAA
  }
}, 50)

const input = ref(null)

function getRoutes() {
  var routes = [];
  router.getRoutes().forEach(element => {
    var route = AAAAAAAA + '/' + element.name;
    routes.push(route.toLowerCase());
  });
  return routes;
}

function focusOnInput() {
  input.value.focus()
}

function checkSubmit(e){
  if (!treatedRoutes.includes(model.value.toLowerCase())){
    console.log('ERROR');
    e.preventDefault();
    return;
  }
  router.push({ name: model.value.replace(AAAAAAAA + '/', '').toLowerCase() });
  e.preventDefault();
}

const [model] = defineModel({ default: AAAAAAAA })
</script>

<template>
  <div class="item">
    <div class="details">
      <h3 @click="focusOnInput">
        {{ model }}
      </h3>
      <div class="input">
        <form @submit="checkSubmit">
          <input type="text" ref="input" v-model="model" @input="onInput" />
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped>
h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--terminal-heading-color-text);
}

input {
  opacity: 0;
  filter: alpha(opacity=0);
}

div {
  .input {
    width: 0;
    overflow: hidden;
  }
}
</style>
