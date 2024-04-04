<template>
  <div class="container-home">
    <HeaderVue />
    <ApresentationVue />
  </div>
</template>

<script setup>
import HeaderVue from "../components/HeaderVue.vue";
import ApresentationVue from "../components/ApresentationVue.vue";
</script>

<style scoped>
.container-home {
  display: grid;
  grid-template-areas:
      "header"
      "main"
      "footer";
  grid-template-rows: 14% 71% 15%;
  height: 100vh;
}
</style>