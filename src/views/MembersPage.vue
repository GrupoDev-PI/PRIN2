<script setup>
import { ref, onMounted } from 'vue';
import axios from 'axios'

const dadosMembros = ref([]);

onMounted(async () => {
  const { data } = await axios.get('http://localhost:3000/membros');
  console.log(data);
  dadosMembros.value = data
})
</script>

<template>
  <h1>Member's Page</h1>
  <div class="profiles-container">
    <div v-for="(membro, membroIndex) in dadosMembros" class="profile-content">
      <div><span class="dot"></span></div>
      <div>
        <h2>Nome do cara: {{ membro.nome }}</h2>
        <p>insta: {{ membro.instagram }}</p>
        <p>github: {{ membro.github }}</p>
    </div>
    </div>
  </div>
</template>

<style scoped>
h1 {
  text-align: center;
}
.profiles-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.profile-content {
  width: 800px;
  height: 400px;
  margin: 10px;
  border: 1px solid #ccc;
  border-radius: 8px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: flex-start;
  justify-content: space-between;
  padding: 30px;
}

.profile-content div{
    height: 100%;
    width: 100%;
    text-align: center;
}



.dot {
  height: 13vw;
  width: 13vw;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
}
</style>
