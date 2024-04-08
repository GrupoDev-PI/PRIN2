<script setup></script>

<template>
  <title>Página de Contato</title>
    <section class="contacts">
      <div class="container">
        <h2>Contate-nos</h2>
        <div class="contact-wrapper">
          <div class="contact-form">
            <h3>Mande uma mensagem</h3>
            <form>
              <div class="form-group">
                <input type="text" name="nome" placeholder="Seu nome">
              </div>
              <div class="form-group">  
                <input type="email" name="email" placeholder="Seu email">
              </div>
              <div class="form-group">  
                <textarea name="mensagem" placeholder="Sua mensagem"></textarea>
              </div>
              <button type="submit">Mande mensagem</button>
            </form>
          </div>
          <div class="contact-info">
            <h3>Informações de contato</h3>
            <p>+11 1234-5678</p>
            <p>+11 1234-5678</p>
            <p>+11 1234-5678</p>
            <p>+11 1234-5678</p>
            <p>+11 1234-5678</p>
            <p>luiz.fernando.251107@gmail.com</p>
            <p>nicolassteffenspereira@gmail.com</p>
            <p>luiz.fernando.251107@gmail.com</p>
            <p>luiz.fernando.251107@gmail.com</p>
            <p>luiz.fernando.251107@gmail.com</p>
          </div>
        </div>

      </div>

    </section>



</template>
<style>

  .contacts{
    display: grid;
    height: 100vh;
    place-items: center;

    color: #ffffff;
  }
  .container{
    max-width: 800px;
    margin:0 auto;
    align-items: center;
    background-color: rgb(102, 102, 102)
  }
   h2{
    text-align: center;
    font-size: 36px;
    margin-bottom: 40px;
    color: #ffffff;
  }
  .contact-wrapper{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 30px;
  }
  .contact-form{
    text-align: left;
  }
  .contact-form h3{
    font-size: 24px;
    margin-bottom: 20px;
  }
  .form-group{
    margin-bottom: 20px;
  }
  input, textarea{
    width: 100%;
    padding: 12px;
    border-radius: 8px;
    border: none;
  }
  input:focus,
  textarea:focus{
    outline: none;
    box-shadow: 0 0 8px ;
  }
  button{
    display: inline-block;
    padding: 12px 24px;
    border: none;
    cursor: pointer;
    background-color: #26c52e;
  }
  button{
    display: inline-block;
    padding: 12px 24px;
    border: none;
    cursor: pointer;
    transition: 0.3s ease;
    border-radius: 10px;
    text-align: center;
  }
  button:hover{
    background-color: #1713d1;
  }
  .contact-info{
    text-align: left;
  }
  .contact-info h3{
    font-size: 24px;
    margin-bottom: 20px;
  }
  .contact-info p{
    margin-bottom: 10px;
  }
  .contact-info i{
    color:#4caf50;
    margin-right: 10px;
  }

@media screen and(max-width: 768px){
  .container{
    padding: 20px;
  }
  .contact-wrapper{
    grid-template-columns: 1fr;
  }
}
</style>
