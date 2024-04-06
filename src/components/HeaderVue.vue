<template>
    <header>
        <nav class="container-nav">
            <ul class="list-nav">
                <li><img src="/logo_pi.png" alt="" class="logo"></li>
                <li class="link-navegation">Membros</li>
                <li class="link-navegation">Contato</li>
                <li class="link-navegation">Projetos</li>
            </ul>
            <ul class="list-auth">
                <li class="link-authentication">Login</li>
                <li class="link-authentication button-register">Register</li>
            </ul>
        </nav>
    </header>
</template>

<script setup>

</script>

<style scoped>
header {
    grid-area: header;
    background-color: #C2C2C2;
    font-family: "Inter", sans-serif;
}

.container-nav {
    display: flex;
    justify-content: space-between;
    padding: 10px 35px;
}

.list-nav, .list-auth {
    display: flex;
    align-items: center;
    gap: 35px;
    list-style: none;
    font-size: 20px;
}

.list-auth {
    gap: 25px;
}

.logo {
    position: relative;
    top: 5px;
    width: 100px;
}

.button-register {
    background-color: #000;
    color: #FDFDFD;
    border: none;
    border-radius: 5px;
    padding: 8px 16px;
    font-size: 20px;
    font-weight: 500;
    transition: .4s ease-in-out;
    cursor: pointer;
}

.button-register:hover {
    background-color: #FDFDFD;
    color: #000;
    font-weight: 500;
}
</style>