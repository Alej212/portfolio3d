<template>
    <TresCanvas class="tres-canvas" :alpha="true">
        <TresPerspectiveCamera :look-at="[0,0,0]"/>
        <OrbitControls/>
                <Suspense>
                    <ContentFooterDeerBody/>
                </Suspense>
            <!-- <TresGridHelper/> -->
            <TresAmbientLight :intensity="0.1" />
        <TresDirectionalLight cast-shadow :position="[0, 15, 0]" :intensity="4" />
   </TresCanvas>
</template>

<script setup lang="ts">
import { TresCanvas } from '@tresjs/core';
</script>

<style scoped lang="scss"></style>