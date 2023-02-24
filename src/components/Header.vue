<template>
  <header>
    <h2 class="title">{{ wordValue ? wordValue : 'Word Hunt' }}</h2>
    <div class="input-wrap">
      <input type="text" placeholder="search a Word" v-model="wordValue" @input="$emit('update:modelValue', $event.target.value)" />
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
const wordValue = ref()
difinEmits: ['update:modelValue']
</script>

<style scoped lang="scss">
header {
  height: 30vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  h2 {
    font-size: 7vh;
    font-weight: 100;
    @media (max-width: 1000px) {
      font-size: 11vw;
    }
  }
  .input-wrap {
    input {
      width: 50vw;
      border: none;
      background-color: #515156;
      border-bottom: 1px solid rgb(197, 188, 188);
      padding: 5px;
      font-size: 18px;
      color: white;
      &:focus {
        outline: none;
        border-bottom: 1px solid rgb(255, 255, 255);
      }
      &::placeholder {
        color: rgba($color: #fff, $alpha: 0.5);
      }
    }
  }
}
</style>
