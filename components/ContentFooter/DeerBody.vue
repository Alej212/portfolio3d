<template>
    <primitive :object="model" :scale="0.0025" :position="[0,-2,0]"/>
</template>

<script setup lang="ts">
import { onMounted } from 'vue';
import { useGLTF } from '@tresjs/cientos';
import * as THREE from 'three';

const { scene: model, nodes, animations, materials } = await useGLTF('/deertwo/scene.gltf')


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
        model.rotation.y += 0.015; // Ajusta este valor para cambiar la velocidad de rotación
        requestAnimationFrame(animate);
    }

    animate();
});
</script>

<style scoped lang="scss"></style>