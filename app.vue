<template>
  <header>
    <MenuBar></MenuBar>
  </header>
  <main>
    <NuxtPage/>
  </main>
  <footer>
    <ContentFooter/>
  </footer>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  //background-color: hsla(0, 0%, 0%, 20%);
  z-index: 4;
}

footer {
  background-color: hsl(0, 0%, 9%);
}
</style>
