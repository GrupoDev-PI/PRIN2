<template>
    <header>
        <div class="container-header">
            <nav class="container-nav">
                <ul class="list-nav">
                    <li class="link-navegation">Membros</li>
                    <li class="link-navegation">Contato</li>
                    <li class="link-navegation">Projetos</li>
                    <li>
                        <button class="button-login">Login</button>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script setup>

</script>

<style scoped>
header {
    font-family: "Inter", sans-serif;
}
.container-header {
    display: flex;
    justify-content: flex-end;
    margin-right: 20px;
}

.container-nav {
    padding: 60px;
}

.list-nav {
    display: flex;
    gap: 35px;
    list-style: none;
}

.button-login {
    
}
</style>