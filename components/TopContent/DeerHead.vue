<template>
    <primitive :object="model" :position="[-0.5,-1,0.8]" :rotation="[1,0,0]" :scale="0.025"/>
</template>
<!-- 
<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue';
import { useGLTF } from '@tresjs/cientos';
import * as THREE from 'three';

const { scene: model, nodes, animations, materials } = await useGLTF('/deer.gltf')

let mouse = { x: 0, y: 0 };

window.addEventListener('mousemove', (event) => {
  mouse.x = (event.clientX / window.innerWidth) * 2 - 1;
  mouse.y = -(event.clientY / window.innerHeight) * 2 + 1;
});

onMounted(() => {
    for (const material of Object.values(materials)) {
        if (material instanceof THREE.MeshStandardMaterial) {
            material.color.set(0xbf3149); // Color neón
            material.emissive.set(0xbf3149); // Color de emisión
            material.emissiveIntensity = 1; // Intensidad de emisión
            material.metalness = 0; // Metalicidad
            material.roughness = -5; // Rugosidad
        }
    }
    const animate = () => {
        model.rotation.y = mouse.x;
        model.rotation.x = mouse.y;
        requestAnimationFrame(animate);
    }

    animate();
});
</script> -->

<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue';
import { useGLTF } from '@tresjs/cientos';
import * as THREE from 'three';

const { scene: model, nodes, animations, materials } = await useGLTF('/deer.gltf')

let mouse = new THREE.Vector2();
let targetRotation = new THREE.Vector2();

window.addEventListener('mousemove', (event) => {
  mouse.x = (event.clientX / window.innerWidth) * 2 - 1;
  mouse.y = -(event.clientY / window.innerHeight) * 2 + 1;
});

onMounted(() => {
    for (const material of Object.values(materials)) {
        if (material instanceof THREE.MeshStandardMaterial) {
            material.color.set(0xbf3149); // Color neón
            material.emissive.set(0xbf3149); // Color de emisión
            material.emissiveIntensity = 1; // Intensidad de emisión
            material.metalness = 0; // Metalicidad
            material.roughness = -5; // Rugosidad
        }
    }

    const animate = () => {
        targetRotation.x = mouse.y;
        targetRotation.y = mouse.x;

        // Interpola la rotación del modelo hacia la rotación objetivo
        model.rotation.x = THREE.MathUtils.lerp(model.rotation.x, targetRotation.x, 0.1);
        model.rotation.y = THREE.MathUtils.lerp(model.rotation.y, targetRotation.y, 0.1);

        requestAnimationFrame(animate);
    }

    animate();
});
</script>

<style scoped lang="scss"></style>