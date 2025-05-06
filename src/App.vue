<script setup>
import { ref } from 'vue';
const item = ref([
{
        id: 1,
        titulo: 'Chain of Iron: Volume 2',
        autor: 'Cassandra Clare',
        preco: 23.24,
        capa: "public/imagens/livro1.png",
    },
    {
        id: 2,
        titulo: 'Chain of Thorns',
        autor: 'Cassandra Clare',
        preco: 23.24,
        capa: "public/imagens/livro2.png",
    },
    {
        id: 3,
        titulo: 'City of Fallen Angels',
        autor: 'Cassandra Clare',
        preco: 13.94,
        capa: "public/imagens/livro3.png",
    },
    {
        id: 4,
        titulo: 'Nona the Ninth',
        autor: 'Cassandra Clare',
        preco: 16.84,
        capa: "public/imagens/livro4.png",
    },
    {
        id: 5,
        titulo: 'Harlem Shuffle',
        autor: 'Colson Whitehead',
        preco: 26.92,
        capa: "public/imagens/livro5.png",
    },
    {
        id: 6,
        titulo: 'Two Old Women',
        autor: 'Velma Wallis', 
        preco: 13.95,
        capa: "public/imagens/livro6.png",
    },
    {
        id: 7,
        titulo: 'Carrie Soto Is Back',
        autor: 'Taylor Jenkins Reid',
        preco: 26.04,
        capa: "public/imagens/livro7.png",
    },
    {
        id: 8,
        titulo: 'Book Lovers',
        autor: 'Emily Henry',
        preco: 15.81,
        capa: "public/imagens/livro8.png",
    },
])
</script>

<template>
<main>
  <header>
    <div class="topo">
      <div class="if">
        <p>IFbooks</p>
        </div>
        <span class="barra"></span>
        <div>
        <p class="apreco">Apreço a <br>leitura</p>
      </div>
      <div class="pesquisa">
        <input type="text" placeholder="Pesquisar">
        <i class="fa-solid fa-magnifying-glass"></i>
      </div>
    <div class="itens">
        <nav>
            <a href="#">Termos</a>
        
            <a href="#">Devoluções</a>
        
            <a href="#">Envio</a>
          
            <a href="#">Equipe</a>
        </nav>
    </div>
    <div class="icons">
      <i class="fa-solid fa-cart-shopping"></i>
      <span></span>
      <i class="fa-solid fa-heart"></i>
      <span></span>
      <i class="fa-solid fa-user"></i>
    </div>
    </div>
    <hr>
  </header>
  <section class="inico">

  <div class="pagina1">
        <div class="mudar">
          <p class="autor">Autor de Abril</p>
          <h1>Eric-Emanuel Schmitt </h1>
          <p>Eric-Emmanuel Schmitt has been awarded more than 20 <br> literary prizes and distinctions, and in 2001 he received the <br> title of Chevalier des Arts et des Lettres. His books have been <br> translated into over 40 languages.</p>
          <a href="#">Acessar página do livro</a>
        </div>  
        <div class="schmitt">
          <img src="/public/imagens/book.png" alt="book.png" style="display: block;">
        </div>
  </div> 
  </section>
  <section class="mais">
    <div class="itenss">
      <div class="frete">
        <i class="fa-solid fa-truck"></i>
        Frete grátis para SC
      </div>
      <hr>
      <div>
        <i class="fa-solid fa-star"></i>
        Livros recomendados
      </div>
      <hr>
      <div>
        <i class="fa-solid fa-book-open"></i>
        Mais vendidos
      </div>
    </div>
    <hr>
  </section>
  <section class="lancamentos">
    <h2 class="rapido">Lançamentos</h2>
    <div class="cima">
      <div>
        <img src="/public/imagens/Livro1.png" alt="Livro1.png">
        <h2>Chain of Iron: Volume 2</h2>
        <p>Cassandra Clare</p>
        <p>R$23.24</p> 
        <a href="#"><i class="fa-solid fa-cart-shopping"></i>comprar</a>
      </div>
      <div>
        <img src="/public/imagens/Livro2.png" alt="Livro2.png">
        <h2>Chain of Thorns</h2>
        <p>Cassandra Clare</p>
        <p>R$23.24</p>
        <a href="#"><i class="fa-solid fa-cart-shopping"></i>comprar</a>
      </div>
      
      <div>
        <img src="/public/imagens/Livro3.png" alt="Livro3.png">
        <h2>City of Fallen Angels</h2>
        <p>Cassandra Clare</p>
        <p>R$13.94</p> 
        <a href="#"><i class="fa-solid fa-cart-shopping"></i>comprar</a>
      </div>
      <div>
        <img src="/public/imagens/Livro4.png" alt="Livro4.png">
        <h2>Nona the Ninth</h2>
        <p>Cassandra Clare</p>
        <p>R$16.84</p> 
        <a href="#"><i class="fa-solid fa-cart-shopping"></i>comprar</a>
      </div>
    </div>
    <div class="baixo">
      <div>
        <img src="/public/imagens/Livro5.png" alt="Livro5.png">
        <h2>Harlem Shuffle</h2>
        <p>Colson Whitehead</p>
        <p>R$26.92</p> 
        <a href="#"><i class="fa-solid fa-cart-shopping"></i>comprar</a>
      </div>
      <div>
        <img src="/public/imagens/Livro6.png" alt="Livro6.png">
        <h2>Two Old Women</h2>
        <p>Two Old Women</p>
        <p>R$13.95</p> 
        <a href="#"><i class="fa-solid fa-cart-shopping"></i>comprar</a>
      </div>
      <div>
        <img src="/public/imagens/Livro7.png" alt="Livro7.png">
        <h2>Carrie Soto Is Back</h2>
        <p>Taylor Jenkins Reid</p>
        <p>R$26.04</p> 
        <a href="#"><i class="fa-solid fa-cart-shopping"></i>comprar</a>
      </div>
      <div>
        <img src="/public/imagens/Livro8.png" alt="Livro8.png">
        <h2>Book Lovers</h2>
        <p>Emily Henry</p>
        <p>R$15.81</p> 
        <a href="#"><i class="fa-solid fa-cart-shopping"></i>comprar</a>
      </div>
    </div>
  </section>
</main> 
<footer>
  <div class="ifbooks">
    <h2>IFbooks</h2>
    <i class="fa-brands fa-square-facebook"></i>
    <i class="fa-brands fa-square-instagram"></i>
    <i class="fa-brands fa-square-twitter"></i>
  </div>
  <div class="contato">
    <h2>Contato</h2>
    <i class="fa-solid fa-phone"></i> <p>+55 47 40045263</p>
    <i class="fa-solid fa-clock"></i> <p>8h às 23h - Seg a Sex</p>
    <i class="fa-solid fa-envelope"></i> <p>contato@ifbooks.com</p>
    <img src="/public/imagens/paypal.png" alt="paypal.png">
    <img src="/public/imagens/MasterCard.png" alt="MasterCard.png">
    <img src="/public/imagens/VISA.png" alt="VISA.png">
  </div>
  <div>
    &copy; Alguns direitos reservados. IFbooks 2025. 
  </div>
</footer>
</template>

<style scoped>
  div.topo{
    display: flex;
    margin: 0 10vw;
}
  div.if{
    margin: 1vw 1vw;
  }
  div p.apreco{
    margin: 1vw 1vw;
  }
  div.pesquisa{
    margin: 1vw 4vw; 
  }
  div.pesquisa input {
    width: 20vw;
  }
  div.itens {
    margin: 1vw 2.5vw;
  }
  div.icons {
    margin: 1vw 2vw;
    padding: 0.7vw;
  }
  div.pagina1 {
    display: flex; 
  }
  div.pagina1 div.mudar {
    margin: 4vw 10vw;
  }
  div.pagina1 div.mudar h1{
    font-size: 2.5rem;
  }
  div.pagina1 div.mudar p.autor{
    font-size: 1.3rem;
    color: #27AE60;
    border: #27AE60 solid;
    border-radius: 4px;
    border-width: 2px;
    padding: 3px;
  }
  div.pagina1 div.mudar a {
    text-decoration: none;
    background-color: #27AE60;
    font-size: 1.2rem;
    padding:16px;
    border: #27AE60;
    color: white;
    margin: 3vw 0vw;
  }
  div.pagina1 div.schmitt {
    margin: 4vw 10vw;
  }
  svg{
    width: 20px;
  }
  p.apreco{
    color: #27AE6099;
  }
  div.itens nav a{
    text-decoration: none;
    margin: 20px;
    color: black;
  }
  div.icons i{
    margin: 0 10px 10px 0 ;
  }
  div.icons span{
    border-left: solid 1px;
    margin: 0 10px 20px 0;
  }
  header span{
    border-left: solid 1px;

  }
  section.lancamentos div.cima{
    display: flex;
    padding: 5vw;
    justify-content: space-between;
  }
  section.lancamentos div.baixo{
    display: flex;
    margin: 5vw;
    justify-content: space-between;
    text-decoration: none;
  }
  section.lancamentos div.cima a {
    text-decoration: none;
    border: #27AE60;
    background-color: #27AE60;
    padding: 16px;
    margin: 3vw;
    border-radius: 20px;
    color: white;
  }
  section.lacamentos div.cima div h2{
    font-size: 1.4rem;
  }
  section.lancamentos div.baixo a {
    text-decoration: none;
    border: #27AE60;
    background-color: #27AE60;
    padding: 16px;
    margin: 3vw;
    border-radius: 20px;
    color: white;
  }
  section.mais div.itenss {
    display: flex;
    justify-content: space-between;
    width: 97%;
  }
  section.mais hr{
    border-bottom: solid 20px;
  }
  section.mais div.frete {
    text-align: center;
  }
  section.mais{
    margin: 50px;
  }
  section.mais hr{
    border-bottom: solid 2px;
  }
  section header div.icons{
    color: #27AE60;
  }
  .rapido {
    margin: 6vw 8vw 4vw 8vw;
    font-size: 3rem;
  }
  header div.itens nav a{
    color: #7B7881;
  }
  header hr{
    color: #27AE60;
  }
  footer{
    background-color: #27AE60;
    color: white;
  }
  footer div.ifbooks h2{
    margin: 5vw;
  }
  footer div.ifbooks i {
    margin: 0vw 2vw;
    font-size: 2rem;
  }
  footer div.contato {
   justify-content: right;
  }
</style>
