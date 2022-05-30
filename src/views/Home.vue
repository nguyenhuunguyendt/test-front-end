<template>
  <div class="main-container">
    <Sidebar />
    <Content />
  </div>
</template>

<script setup>
import Sidebar from "../components/Sidebar.vue";
import Content from "../components/Content.vue";
</script>
<style scoped>
.main-container {
  max-width: 1918;
}
</style>
