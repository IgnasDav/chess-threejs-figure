<script setup lang="ts">
import { onMounted, ref, useTemplateRef } from 'vue'

const btnRef = useTemplateRef('btn')
const playAmount = ref<number>(0)

function play(): void {
  if (playAmount.value < 1) {
    playAmount.value = playAmount.value + 1
    const audio = new Audio(
      'https://raw.githubusercontent.com/IgnasDav/chess-threejs-figure/main/public/song.mp3',
    )
    audio.play()
  }
}

onMounted(() => {
  window.addEventListener('click', play)
  window.addEventListener('touchstart', play)
})
</script>
<template>
  <button @click="play" ref="btn" style="visibility: hidden">Play</button>
</template>
