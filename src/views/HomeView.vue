<script setup>
import AAAAAAAAAInput from '../components/AAAAAAAAInput.vue'
import AAAAAAAAAFooter from '../components/AAAAAAAAAFooter.vue'
</script>

<template>
  <main>
    <div class="centered">
      <div class="input">
        <AAAAAAAAAInput />
      </div>
      <div class="img">
        <img class="marsh" src="../assets/imgs/AAAAAAAAMarsh.jpeg">
      </div>
    </div>
  </main>
  <footer>
    <AAAAAAAAAFooter/>
  </footer>
</template>


<style> 
  .marsh{
    max-width: 400px;
    max-height: 400px;
  }
</style>