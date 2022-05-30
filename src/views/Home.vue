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
  display: flex;
  flex-wrap: wrap;
  margin: 0 auto;
  max-width: 1918px;
}
@media (min-width: 740px) and (max-width: 1023px) {
  .main-container {
    flex-direction: column;
    align-items: center;
    margin: 0 auto;
    max-width: 1023px;
  }
}
/*mobile  */
@media (max-width: 739px) {
  .main-container {
    /* flex-direction: column; */
    /* align-items: center; */
    display: block;
    margin: 0 auto;
    max-width: 739px;
  }
}
</style>
