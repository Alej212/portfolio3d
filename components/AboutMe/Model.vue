<template>
    <TresCanvas class="tres-canvas" :alpha="true">
        <TresPerspectiveCamera :position="[-3,1,5]" :rotation="[0,0,0]" :look-at="[0,0,0]"/>
                <Suspense>
                    <AboutMeDeerO/>
                </Suspense>
            <TresAmbientLight :intensity="0.1" />
        <TresDirectionalLight cast-shadow :position="[3, -4, 2]" :intensity="8" />
   </TresCanvas>
</template>

<script setup lang="ts">
import { TresCanvas } from '@tresjs/core';
</script>

<style scoped lang="scss">
.tres-canvas {
    width: 100%;
    height: 100%;
}
</style>