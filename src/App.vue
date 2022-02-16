<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import readMore from './components/ReadMore.vue'
let lengthText = 100;
const textCard = `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vitae
  massa ipsum. Maecenas mattis congue metus vel fringilla. Praesent id arcu posuere, cursus metus et,
  venenatis risus. Maecenas sed nunc volutpat, tempus mi sed, tincidunt velit. In malesuada interdum bibendum.
  Maecenas sed porttitor nulla, et feugiat libero. Vivamus hendrerit enim sed sodales lobortis. Ut egestas vehicula
  condimentum. Fusce varius libero vel diam bibendum,
  vel porttitor arcu pharetra. Donec vestibulum venenatis arcu, id luctus eros lacinia vitae. Maecenas vitae sapien ipsum.`
</script>

<template>
  <img alt="Vue logo" src="./assets/logo.png"/>
  <readMore :lengthText="lengthText" text-title="app card" :text-card="textCard"/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
