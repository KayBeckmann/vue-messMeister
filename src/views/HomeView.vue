<template>
  <div class="home">
    <div class="count">{{ counterStore.count }}</div>
    <div class="buttons">
      <button @click="counterStore.decreaseCount">-</button>
      <button @click="counterStore.increaseCount">+</button>
    </div>
    <div>
      The counter is: {{ counterStore.oddOrEven }}
    </div>
  </div>
  <hr>
  <div>
    <h3>Edit counter:</h3>
    <input 
    v-model="counterStore.count"
    type="number"
    min="0"
    >
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter'

const counterStore = useCounterStore()

</script>

<style scoped>
.count{
  font-size: 60px;
  margin: 20px;
}
.buttons{
  font-size: 40px;
  margin: 10px;
}
</style>