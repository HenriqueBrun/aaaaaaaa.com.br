<script setup>
import AAAAAAAAAInput from '../components/AAAAAAAAInput.vue'
import AAAAAAAAAFooter from '../components/AAAAAAAAAFooter.vue'
</script>

<template>
  <main>
    <div class="centered">
      <AAAAAAAAAInput/>
      <div class="list">
        <p class="list-item">/home</p>
        <p class="list-item">/about</p>
        <p class="list-item">/help</p>
      </div>
    </div>
  </main>
  <footer>
    <AAAAAAAAAFooter/>
  </footer>
</template>

<style>

.list-item{
  padding-top: .03em;
}

</style>