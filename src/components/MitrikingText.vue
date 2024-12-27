<script setup lang="ts">
import { useTexture } from '@tresjs/core'
import { Text3D } from '@tresjs/cientos'
const matcapTexture = await useTexture([
  'https://raw.githubusercontent.com/Tresjs/assets/main/textures/matcaps/7.png',
])
</script>

<template>
  <Text3D
    :position="[-1, 0, -3]"
    ref="textRef"
    font="https://raw.githubusercontent.com/Tresjs/assets/main/fonts/FiraCodeRegular.json"
  >
    Mitriking
    <TresMeshMatcapMaterial :matcap="matcapTexture" color="yellow" />
  </Text3D>
</template>
