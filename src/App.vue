<script setup lang="ts">
import Content from "./components/Content.vue";
import Feature from "./components/Feature.vue";
</script>

<template>
  <Content>
    <Feature />
  </Content>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
