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
      <div class="socialMedia" >
        <h2>{{ membro.nome }}</h2>
        <p>{{ membro.instagram }}</p>
        <p>{{ membro.github }}</p>
        <button>hdsjifbsdf</button>
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
  height: 350px;
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
}

.profile-content div {
  height: 100%;
  width: 100%;
  text-align: center;
}

button {
  background-color: #4caf50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  cursor: pointer;
  width: 100%;
}

.profile-content img {
  height: 13vw;
  width: 13vw;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
}
</style>
