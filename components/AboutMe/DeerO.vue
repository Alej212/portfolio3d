<template>
    <primitive :object="model" :position="[-3.5,0,0]" :scale="0.5"/>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';
import { useAnimations } from '@tresjs/cientos'
import * as THREE from 'three';


const { scene: model, nodes, animations, materials } = await useGLTF('/deer/scene.gltf')

const { actions, mixer } = useAnimations(animations, model)

let currentAction = actions.Idle

onMounted(() => {
  currentAction.play();
});

onMounted(() => {
    for (const material of Object.values(materials)) {
        if (material instanceof THREE.MeshStandardMaterial) {
            material.color.set(0xbf3149); // Color neón
            material.emissive.set(0xbf3149); // Color de emisión
            material.emissiveIntensity = 1; // Intensidad de emisión
            material.metalness = 0; // Metalicidad
            material.roughness = 0; // Rugosidad
        }
    }
});
// function changeAnimation('Run') {
//   currentAction.fadeOut(0.5);
//   currentAction = actions[name];
//   currentAction.reset().fadeIn(0.5).play();
// }

console.log(animations)
</script>

