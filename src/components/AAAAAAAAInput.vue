<script setup>
import { useDebounceFn } from '@vueuse/core'
import { ref, computed } from 'vue'

const routes = 'AAAAAAAA/Home'
const AAAAAAAA = 'AAAAAAAA'

const onInput = useDebounceFn((e) => {
  if (!routes.includes(model.value) || !model.value.includes(AAAAAAAA)) {
    model.value = AAAAAAAA
  }
}, 50)

const input = ref(null)

function focusOnInput() {
  input.value.focus()
}

const [model] = defineModel()
</script>

<template>
  <div class="item">
    <div class="details">
      <h3 @click="focusOnInput">
        {{ model }}
      </h3>
      <div class="input">
        <input type="text" ref="input" v-model="model" @input="onInput" />
      </div>
    </div>
  </div>
</template>

<style scoped>
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

.item {
  margin-top: 2rem;
  display: flex;
  position: relative;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 0.4rem 0 1rem calc(var(--section-gap) / 2);
  }

  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
