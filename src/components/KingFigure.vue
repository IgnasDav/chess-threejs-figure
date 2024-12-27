<script setup lang="ts">
import { useGLTF } from '@tresjs/cientos'

const path =
  'https://raw.githubusercontent.com/IgnasDav/chess-threejs-figure/main/public/mitrikas2.glb'

const { scene } = await useGLTF(path, { draco: false })
</script>

<template>
  <primitive :object="scene" />
</template>
