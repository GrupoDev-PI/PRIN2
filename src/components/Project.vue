<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'

const Projetos = ref()

onMounted(async () => {
  const { data } = await axios.get('http://localhost:3000/projetos')
  console.log(data)
  Projetos.value = data
})
</script>
<template>
  <section class="project">
    <div class="container">
      <div v-for="(projeto, projetoIndex) in Projetos" :key="projetoIndex" class="project-content">
        <div class="project-image">
          <img :src="projeto.imagem" alt="Project 1" />
        </div>
        <div class="project-info">
          <h2>{{ projeto.nome }}</h2>
          <p>{{ projeto.descricao}}</p>
          <a href="https://trabalho-gnc.vercel.app/" class="btn">Ver Projeto</a>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
@import '../assets/scss/components/_project1.scss';
</style>