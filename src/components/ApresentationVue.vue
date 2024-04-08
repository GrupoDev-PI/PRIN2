<template>
    <main>
        <div class="container-saudations">
            <h1 class="title">Olá, tudo bem?</h1>
            <p class="saudations">Saudosamente, damos as boas-vindas ao <br> <span class="tprojects">The Projects!</span> </p>
        </div>

        <div class="cards-container">
            <div class="cards-top">
                <div class="cards">
                    <img src="/home/contato.jpg" alt="" class="img-cards">
                    <h2 class="h2-info-card">Contatos</h2>
                    <p class="p-info-card">Fale conosco através dos nossos contatos</p>
                </div>
                <div class="cards">
                    <img src="/home/membros.jpg" alt="" class="img-cards">
                    <h2 class="h2-info-card">Membros</h2>
                    <p class="p-info-card">Conheça o time da The Projects</p>
                </div>
            </div>

            <div class="cards-bottom">
                <img src="/home/projetos.jpeg" class="img-card-bottom" alt="">
                <h2 class="h2-info-card">Projetos</h2>
                <p class="p-info-card">Nossos principais projetos estão aqui.</p>
            </div>
        </div>
    </main>
</template>

<script setup>

</script>

<style scoped>
main {
    margin: 5rem 3rem 5rem 3rem;
}

.title {
    font-family: "Inter", sans-serif;
    font-size: 50px;
}

.saudations {
    margin-top: 5px;
    font-size: 24px;
    color: #828282;
}

.tprojects {
    font-size: 30px;
    color: #000;
}

.cards-container {
    display: flex;
    flex-direction: column;
    margin-top: 30px;
}

.cards-top {
    display: flex;
    justify-content: space-between;
    gap: 20px;
}

.cards-bottom {
    margin-top: 30px;
    width: 100%;
}

.cards {

}

.img-cards {
    border-radius: 5px;
    width: 100%;
}

.img-card-bottom {
    border-radius: 5px;
    width: 100%;
}

.h2-info-card {
    margin-top: 10px;
    margin-left: 2px;
    font-size: 1.2rem;
    font-family: "Inter", sans-serif;
    font-weight: 400;
}

.p-info-card {
    color: #828282;
    font-size: 0.9rem;
    margin-top: 5px;
    margin-left: 2px;
    font-family: "Inter", sans-serif;
}
</style>