<script setup>
import { ref } from 'vue'

const item = ref([
  {
    id: 1,
    titulo: 'Chain of Iron: Volume 2',
    autor: 'Cassandra Clare',
    preco: 23.24,
    capa: "public/imagens/Livro1.png",
    quantidade: 1,
  },
  {
    id: 2,
    titulo: 'Chain of Thorns',
    autor: 'Cassandra Clare',
    preco: 23.24,
    capa: "public/imagens/Livro2.png",
    quantidade: 1,
  },
  {
    id: 3,
    titulo: 'City of Fallen Angels',
    autor: 'Cassandra Clare',
    preco: 13.94,
    capa: "public/imagens/Livro3.png",
    quantidade: 1,
  },
  {
    id: 4,
    titulo: 'Nona the Ninth',
    autor: 'Cassandra Clare',
    preco: 16.84,
    capa: "public/imagens/Livro4.png",
    quantidade: 1,
  },
  {
    id: 5,
    titulo: 'Harlem Shuffle',
    autor: 'Colson Whitehead',
    preco: 26.92,
    capa: "public/imagens/Livro5.png",
    quantidade: 1,
  },
  {
    id: 6,
    titulo: 'Two Old Women',
    autor: 'Velma Wallis',
    preco: 13.95,
    capa: "public/imagens/Livro6.png",
    quantidade: 1,
  },
  {
    id: 7,
    titulo: 'Carrie Soto Is Back',
    autor: 'Taylor Jenkins Reid',
    preco: 26.04,
    capa: "public/imagens/Livro7.png",
    quantidade: 1,
  },
  {
    id: 8,
    titulo: 'Book Lovers',
    autor: 'Emily Henry',
    preco: 15.81,
    capa: "public/imagens/Livro8.png",
    quantidade: 1,
  },
])

const carrinhoVisivel = ref(false)
const carrinho = ref([])

function toggleCarrinho() {
  carrinhoVisivel.value = !carrinhoVisivel.value
}

function adicionarAoCarrinho(livro) {
  const itemExistente = carrinho.value.find(i => i.id === livro.id)
  if (itemExistente) {
    itemExistente.quantidade++
  } else {
    carrinho.value.push({ ...livro, quantidade: 1 })
  }
}
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
      <i class="fa-solid fa-cart-shopping" @click="toggleCarrinho"></i>
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
      <div v-for="livro in item" :key="livro.id" class="livro">
          <img :src="livro.capa" :alt="livro.titulo" />
          <h2>{{ livro.titulo }}</h2>
          <p>{{ livro.autor }}</p>
          <p>R$ {{ livro.preco.toFixed(2) }}</p>
          <a href="#" @click.prevent="adicionarAoCarrinho(livro)">
            <i class="fa-solid fa-cart-shopping"></i> comprar
          </a>
      </div>
    </div>
  </section>
</main>
<div v-if="carrinhoVisivel" class="carrinho">
    <button class="fechar" @click="toggleCarrinho">Fechar</button>
    <h2>Meu Carrinho</h2>
    <ul>
      <li v-for="item in carrinho" :key="item.id">
        {{ item.titulo }} - {{ item.quantidade }}x R${{ item.preco.toFixed(2) }}
      </li>
    </ul>
    <p>
      Total: R$
      {{ carrinho.reduce((total, item) => total + item.preco * item.quantidade, 0).toFixed(2) }}
    </p>
  </div>
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
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 2rem;
    padding: 2rem;
  }
  .livro {
  border: 1px solid #ccc;
  padding: 1rem;
  text-align: center;
}
.livro a {
  display: block;
  margin-top: 1rem;
  background: #27ae60;
  color: white;
  padding: 0.5rem 1rem;
  text-decoration: none;
  border-radius: 10px;
}
  section.lancamentos div.baixo{
    display: flex;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 2rem;
    padding: 2rem;
  }
  section.lancamentos div.cima a {
    text-decoration: none;
    border: #27AE60;
    background-color: #27AE60;
    padding: 16px;
    margin: 3vw;
    border-radius: 20px;
    color: white;
    flex-wrap: nowrap;
  }
  section.lacamentos div.cima div h2{
    font-size: 1.4rem;
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
  .carrinho {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: white;
  z-index: 2000;
  padding: 2rem;
  overflow-y: auto;
}

.carrinho h2 {
  margin-top: 0;
}

.carrinho .fechar {
  position: absolute;
  top: 1rem;
  right: 1rem;
  padding: 0.5rem 1rem;
  background: #c0392b;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}

</style>
