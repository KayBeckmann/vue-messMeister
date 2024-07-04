<template>
  <div class="about">
    <h1>ABOUT</h1>
    <button @click="counterStore.increaseCount">
      {{ counterStore.count }}
    </button>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter'

const counterStore = useCounterStore()

</script>

<style scoped>
.about{
  font-size: 60px;
  margin: 20px;
}
button{
  font-size: 50px;
  margin: 25px;
  padding: 25px;
}
</style>