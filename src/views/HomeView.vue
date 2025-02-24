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
        <!-- LightWidget WIDGET -->
        <script src="https://cdn.lightwidget.com/widgets/lightwidget.js"></script>
        <iframe src="//lightwidget.com/widgets/28ec89879ef6532493e13a390d96b960.html"
                scrolling="no" 
                allowtransparency="true" 
                class="lightwidget-widget" 
                style="width:100%;border:0;overflow:hidden;">
        </iframe>
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
