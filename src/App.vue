<template>

<div class="flex justify-center items-center h-screen">
  <div class="text-center">
    <span class="text-gray-700 ml-9 text-4xl">The Count is</span>
    <p class="text-6xl text-gray-500 font-bold">{{ count }}</p>
    <div class="flex justify-center gap-4 mt-4">
      <button @click='increment'  class="bg-green-400 px-4 py-2">+</button>
      <button @click="decrement"  class="bg-red-400 px-4 py-2">-</button>
    </div>
    <button  @click="count=0" class="bg-red-500 px-4 mt-3 rounded-sm text-gray-200">Reset</button>
  </div>
</div>

</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

const increment = () => {
  count.value++
}

const decrement = () => {
  count.value--
}

const reset = () => {
  count.value = 0
}


</script>