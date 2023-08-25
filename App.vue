<script setup>
import { ref } from 'vue'

const hello = ref(true)
const show = ref(true)
const color = ['black', 'blue', 'green', 'pink']
const input = ref('')
</script>

<template>
  <div>
    <button @click="hello = !hello">Greeting</button>
    <br>
    <h1 v-if="hello">Hello</h1>
    <h1 v-else>Byebye</h1>

    <br>
    <button @click="show = !show">Show</button>
    <br>
    <h1 v-show="show">Yay!!</h1>
    <br>
    <br>
  </div>
  <div>
    <h1>My Favorite Color</h1>
    <br>
    <ul>
    <li v-for="x in color">{{ x }}</li>
    </ul>
    <br>
  </div>

  <div>
    <p>What you've input: {{ input }}</p>
    <input v-model="input" placeholder="Input">
  </div>
</template>

<style scoped>

button{
margin-bottom: 20px;
margin-top: 20px;
}

div{
  margin: auto;
  text-align: center;
}

</style>
