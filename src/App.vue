<script setup>
import { ref } from 'vue'

const message = "hello world"
const rawHtml = "<li>halooo</li>"
const link = "https://smkassalaambandung.sch.id/"
let a=10
let b=5
let c =a+b
</script>

<template>
  <div v-bind:id="dynamicId" id="app">
   <h1>{{ message }}</h1>

   <span style="color: red" v-html="rawHtml"></span>

    <button :disabled="isButtonDisabled">button</button><br>
    <a v-bind:href="link">situs assalaam</a><br>
    bil1={{ a }}<br>
    bil2={{ b }}<br>
    hasil={{ c }}

  </div>

</template>