<template>
    <TresCanvas class="tres-canvas" :alpha="true">
        <TresPerspectiveCamera :position="[-0.45,-0.400,-4.80]" :rotation="[0,0,0]" :look-at="[0,0,0]"/>
                <Suspense>
                    <TopContentDeerHead/>
                </Suspense>
            <TresAmbientLight :intensity="0.1" />
        <TresDirectionalLight cast-shadow :position="[0, 20, 0]" :intensity="8" />
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