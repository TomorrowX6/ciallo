<template>
  <main>
    <h1>喵喵</h1>
    <md-filled-button @click="playSound">点我</md-filled-button>
  </main>
</template>

<script setup>
import '@material/web/button/filled-button.js'

const audio = new Audio('src/sounds/click.mp3')

function playSound() {
  audio.currentTime = 0
  audio.play()
}
</script>

<style scoped>
md-filled-button {
  margin-top: 16px;
  --md-sys-color-primary: #1a73e8;
}
</style>
