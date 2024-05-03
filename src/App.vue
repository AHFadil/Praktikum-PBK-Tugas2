<script setup>
import { reactive, ref } from 'vue'

const awesome = ref(true) 
const count = ref(0)
const text = ref('')


function increment(){
  count.value++
}

function pencet() {
  awesome.value = !awesome.value
}


</script>

<template>
  <input v-model="text" placeholder="ketik disini">
    <p>{{ text }}</p>
      <button @click="pencet">pencet</button>
      <h3>
      <button @click="increment">input: {{ count }}</button>
      </h3>
    <h1 v-if="awesome">saya melewati jalan bagus</h1>
    <h1 v-else>saya melewati jalan jelek</h1>
</template>
