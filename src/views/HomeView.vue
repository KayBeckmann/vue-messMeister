<template>
  <div class="home">
    <div class="count">{{ count }}</div>
    <div class="buttons">
      <button @click="decreaseCount">-</button>
      <button @click="increaseCount">+</button>
    </div>
    <div>
      The counter is: {{ oddOrEven }}
    </div>
  </div>
</template>

<script setup>
import { computed, ref } from 'vue'

const count = ref(2)

const increaseCount = ()=>{
  count.value++
}

const decreaseCount = ()=>{
  if(count.value > 0){
    count.value--
  }
}

const oddOrEven = computed(()=>{
  if(count.value % 2 === 0){
    return 'even'
  }else{
    return 'odd'
  }
})
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