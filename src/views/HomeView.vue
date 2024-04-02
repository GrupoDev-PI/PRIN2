<template>
  <div class="container-home">
    <HeaderVue />
  </div>
</template>

<script setup>
import HeaderVue from "../components/HeaderVue.vue";
</script>

<style scoped>
.container-home {
  display: grid;
  grid-template-areas:
  "header"
  "main"
  "footer";
  grid-template-rows: 1fr 3fr 2fr;
}
</style>