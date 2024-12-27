<script setup lang="ts">
import { OrbitControls } from '@tresjs/cientos'
import { TresCanvas } from '@tresjs/core'
import KingFigure from './components/KingFigure.vue'
import MitrikingText from './components/MitrikingText.vue'
import AudioPlayer from './components/AudioPlayer.vue'
</script>

<template>
  <TresCanvas clear-color="#fff" window-size>
    <TresPerspectiveCamera :position="[4.7, 2.5, 10]" />
    <OrbitControls />
    <Suspense>
      <TresMesh :position="[-1, 1, 1]">
        <KingFigure />
      </TresMesh>
    </Suspense>
    <Suspense>
      <TresMesh :position="[-1, 3, 1]">
        <MitrikingText />
      </TresMesh>
    </Suspense>
    <TresAmbientLight :intensity="1" />
  </TresCanvas>
  <AudioPlayer />
</template>
