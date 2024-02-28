<script setup>
import { ref } from 'vue'
import AAAAAAAAInput from './AAAAAAAAInput.vue'

const aaaaaaaa = ref('AAAAAAAA')
</script>

<template>
  <AAAAAAAAInput v-model="aaaaaaaa">
    <template #heading>AAAAAAAA</template>
    <template #placeholder>AAAAAAAA</template>
  </AAAAAAAAInput>
</template>
