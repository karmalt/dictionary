<template>
  <div class="container">
    <main>
      <Header v-model="searchWord"></Header>
      <Definition :searchWord="searchWord"></Definition>
    </main>
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Definition from './components/Definition.vue'
import { ref, watch } from 'vue'
const searchWord = ref()
</script>

<style scoped lang="scss">
div.container {
  height: 100vh;
  overflow: hidden;
  background-color: #232324;
  main {
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    color: #fff;
    padding: 1rem;
  }
}
</style>
