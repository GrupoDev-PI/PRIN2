<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'

const projetos = ref()

onMounted(async () => {
  const { data } = await axios.get('http://localhost:3000/projetos')
  console.log(data)
  projetos.value = data
})
</script>
<template>
  <section class="project">
    <div class="container">
      <div v-for="(projeto, projetoIndex) in projetos" :key="projetoIndex" class="project-content">
        <div class="project-image">
          <img :src="projeto.imagem" alt="Project 1" />
        </div>
        <div class="project-info">
          <h2>{{ projeto.nome }}</h2>
          <p>{{ projeto.descricao }}</p>
          <a :href="projeto.linkProject" class="btn">Ver Projeto</a>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
* {
  font-family: 'Inter', sans-serif;
}
.container {
  display: flex;
  justify-content: space-between;
}
.project-content {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 30vw;
  font-family: 'Inter', sans-serif;
  letter-spacing: 0.7px;
  border-radius: 10px;
  background-color: #dfdfdf;
  margin: 10px;
}
.project-content .project-image {
  width: 100%;
  display: flex;
}
.project-content .project-image img {
  width: 100%;
  border-radius: 5px;
  box-shadow: 0 0 12px rgba(0, 0, 0, 0.1);
  height: 200px;
}
.project-info {
  padding: 20px;
  border-radius: 5px;
  margin-bottom: 20px;
}
.project-info h3 {
  font-size: 20px;
  margin-bottom: 10px;
}
.project-info p {
  font-size: 16px;
  margin-bottom: 10px;
}
.project-info a {
  color: #505050;
  text-decoration: none;
  scale: 1.1;
}
.project-info a:hover {
  text-decoration: underline;
  scale: 1.1;
}
.project-info .btn {
  background-color: #dfdfdf;
  border: 1px solid #414141;
  padding: 5px 10px;
  border-radius: 5px;
  margin-top: 10px;
  transition: all 0.3s;
}
.project-info .btn:hover {
  background-color: #505050;
  color: #f9f9f9;
}
</style>