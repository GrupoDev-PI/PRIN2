<script setup>
</script>
<template>
    <header class="header">
        <div class="container">
            <div class="logo">
                <img src="../assets/img/logo.png" alt="The Software Guy" class="logo" />
            </div>
            <nav class="links">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">About</a></li>
                    <li><a href="#">Services</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>
<style scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

.container {
  max-width: 100vw;
  display: flex;
  padding: 0 20px;
}

.header {
  display: flex;
  height: 100px;
  align-items: center;
  background-color: #adadad !important;
}
.header .logo {
  width: 100px;
  height: 100px;
}
.header .links {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.header .links ul {
  display: flex;
  list-style: none;
  display: flex;
}
.header .links ul li {
  margin: 0 15px;
}
.header .links ul li a {
  text-decoration: none;
  color: #000;
  font-size: 1.2rem;
}
.header .links ul li a:hover {
  color: #f00;
  transition: all 0.5s ease-in-out;
}
</style>