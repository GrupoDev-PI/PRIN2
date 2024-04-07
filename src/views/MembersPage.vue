<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'

const dadosMembros = ref([])

onMounted(async () => {
  const { data } = await axios.get('http://localhost:3000/membros')
  console.log(data)
  dadosMembros.value = data
})
</script>

<template>
  <h1>Member's Page</h1>
  <div class="profiles-container">
    <div v-for="(membro, membroIndex) in dadosMembros" class="profile-content">
      <div><img :src="membro.foto" alt="" /></div>
      <div class="socialMedia">
        <h2>{{ membro.nome }}</h2>
        <div class="links">
          <a :href="membro.instaLink" target="_blank">@{{ membro.instagram }}</a>
          <a :href="membro.githubLink">@{{ membro.github }}</a>
        </div>
        <button>Ver mais</button>
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
  width: 41vw;
  height: 18vw;
  margin: 10px;
  border-radius: 8px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: flex-start;
  justify-content: space-between;
  padding: 30px;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
  transition: 0.2s ease-in-out;
}

.profile-content:hover {
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  transform: translateY(-5px);
}

.profile-content div {
  height: 100%;
  width: 100%;
  text-align: center;
}

.socialMedia button {
  background-color: #C4C4C4;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  cursor: pointer;
  width: 100%;
  transition: ease-in-out 0.2s;
}

.profile-content img {
  height: 13vw;
  width: 13vw;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
}

.socialMedia {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.socialMedia button:hover {
  background-color: #686868;
  
}

.links{
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.links a{
  text-decoration: none;
  color: #000;
  font-size: 1.2rem;
}

.links a:hover{
  color: #396d8b;
}

</style>
