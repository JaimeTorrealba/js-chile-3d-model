<script setup lang="ts">
import { TresCanvas } from '@tresjs/core'
import { MouseParallax } from '@tresjs/cientos'
</script>

<template>
    <TresCanvas clear-color="#82DBC5" window-size class="canvas">
        <TresPerspectiveCamera :position="[0, 0, 3]" :look-at="[0, 0, 0]" />
        <TresMesh>
            <TresTorusGeometry :args="[1, 0.5, 16, 32]" />
            <TresMeshBasicMaterial color="orange" />
        </TresMesh>
        <MouseParallax :factor="1" :ease="3" />
        <TresAmbientLight :intensity="1" />
    </TresCanvas>
</template>
<style scoped>
.canvas {
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: -10;
}
</style>