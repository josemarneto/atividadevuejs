<script setup>
import { ref, computed } from 'vue'

const search = ref('')

const items = ref([
  'Livro 1',
  'Livro 2',
  'Livro 3',
])

const filteredItems = computed(() => {
  return items.value.filter(item =>
    item.toLowerCase().includes(search.value.toLowerCase())
  )
})

const valorLivro1 = 23.24;
const valorLivro2 = 23.24;
const valorLivro3 = 13.94;
const valorLivro4 = 16.84;
const valorLivro5 = 26.92;
const valorLivro6 = 13.95;
const valorlivro7 = 26.04;
const valorLivro8 = 15.81;
</script>

<template>
  <header>
    <nav>
      <h1>IFbooks <span>| Apreço a leiitura</span></h1>
      <div class="search">
        <input type="text" v-model="search" placeholder="Buscar" class="barra">
      </div>
  <ul>
    <li>
      Termos
    </li>
    <li>
      Equipe
    </li>
    <li>
      Envio
    </li>
    <li>
      Devoluções
    </li>
    <li>
      <i class="fas fa-shopping-cart"></i> |
    </li>
    <li>
      <i class="fa-solid fa-heart"></i> |
    </li>
    <li>
      <i class="fa-solid fa-user"></i> 
      
      |
    </li>
  </ul>
</nav>
  </header>

  <main>
    <section class="pt1">
      <div class="div1">
        <p>Autor de Abril</p>
        <h2>Eric-Emanuel Schmitt</h2>
        <p>
          Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and in 2001 he received the title of Chevalier des Arts et des Lettres. His books have been translated into over 40 languages.
        </p>
        <a href="Acessar">Acessar página do livro</a>
      </div>
      <div>
        <img src="/public/imagens/image.png" alt="imagem">
      </div>
    </section>
    <section>
      <ul>
        <li>
          <i class="fa-solid fa-truck"></i> Frete Grátis
        </li>
        <li>
          <i class="fa-solid fa-star"></i> Livros recomendados
        </li>
        <li>
          <i class="fa-solid fa-book-open"></i> Mais vendidos
        </li>
        <li>
          <i class="fa-solid fa-magnifying-glass"></i>
        </li>
      </ul>
    </section>
    <section>
      <h2>
        Lançamentos
      </h2>
      <div>
        <img src="/public/imagens/97819821858242.png" alt="">
        <h3>Chain of Iron: Volume 2</h3>
       <ul>
        <li>
          <p>Cassandra Clare</p>
        </li>
        <li>{{ valorLivro1 }}</li>
        <li>
          <a href="Comprar">Comprar</a>
        </li>
       </ul>
        <img src="/public/imagens/97819821858242(1).png" alt="">
        <h3>Chain of Thorns</h3>
        <ul>
          <li>
            <p>Cassandra Clare</p>
          </li>
          <li>{{ valorLivro2 }}</li>
          <li>
            <a href="Comprar">Comprar</a>
          </li>
        </ul>
        <img src="/public/imagens/97819821858242(2).png" alt="">
        <h3>City of Fallen Angels</h3>
        <ul>
          <li>
            <p>Cassandra Clare</p>
          </li>
          <li>
              {{ valorLivro3 }}
          </li>
          <li>
            <a href="Comprar">Comprar</a>
          </li>
        </ul>
        <img src="/public/imagens/97819821858242(3).png" alt="">
        <h3>Nona the Ninth</h3>
        <ul>
          <li>
            <p>Cassandra Clare</p>
          </li>
          <li>
            {{ valorLivro4 }}
          </li>
          <li>
            <a href="Comprar">Comprar</a>
          </li>
        </ul>
      </div>
      <div>
        <img src="/public/imagens/97819821858242(4).png" alt="">
        <h3>Harlem Shuffle</h3>
        <ul>
          <li>
            <p>Colson Whitehead</p>
          </li>
          <li>
            {{ valorLivro5 }}
          </li>
          <li>
            <a href="Comprar">Comprar</a>
          </li>
        </ul>
        <img src="/public/imagens/97819821858242(5).png" alt="">
        <h3>Two Old Women</h3>
        <ul>
          <li>
            <p>Velma Wallis</p>
          </li>
          <li>
            {{ valorLivro6 }}
          </li>
          <li>
            <a href="Comprar">Comprar</a>
          </li>
        </ul>
        <img src="/public/imagens/97819821858242(6).png" alt="">
        <h3>Carrie Soto Is Back</h3>
        <ul>
          <li>
            <p>Taylor Jenkins Reid</p>
          </li>
          <li>
            {{ valorlivro7 }}
          </li>
          <li>
            <a href="Comprar">Comprar</a>
          </li>
        </ul>
        <img src="/public/imagens/97819821858242(7).png" alt="">
        <h3>Book Lovers</h3>
        <ul>
          <li>
            <p>Emily Henry</p>
          </li>
          <li>
            {{ valorLivro8 }}
          </li>
          <li>
            <a href="Comprar">Comprar</a>
          </li>
        </ul>
      </div>
    </section>
  </main>
  <footer>
  <div>
    <h4>IFbooks</h4>
    <ul>
      <li>
        <i class="fa-brands fa-square-facebook"></i>
      </li>
      <li>
        <i class="fa-brands fa-square-instagram"></i>
      </li>
      <li>
        <i class="fa-brands fa-square-twitter"></i>
      </li>
    </ul>
  </div>
  <div>
    <h4>Contato</h4>
    <li>
      <i class="fa-solid fa-phone">+55 47 40045263</i>
    </li>
    <li>
      <i class="fa-solid fa-clock">8h às 23h - Seg a Sex</i>
    </li>
    <li>
      <i class="fa-solid fa-envelope">contato@ifbooks.com</i>
    </li>
  </div>
  <div>
    <ul>
      <li>
        <img src="/public/imagens/MasterCard-Logo-19791.png" alt="">
      </li>
      <li>
        <img src="/public/imagens/paipal1.png" alt="">
      </li>
      <li>
        <img src="/public/imagens/VISA-card-logo-1.png" alt="">
      </li>
    </ul>
    <div>
      <p>&copy; Alguns Direitos Reservados. IFbooks 2025</p>
    </div>
  </div>
  </footer>
</template>

<style scoped>
/*===========Header============*/
header {
	margin: 2vw 5vw 2vw 5vw;
}
header nav ul {
	display: flex;
}
header nav ul li {
	margin: 0 10px 0 10px;
}
header nav div {
	display: flex;
}
header nav div.search {
	margin: 0 10px 0 10px;
}
/*=============Main================*/
main section.pt1 {
	display: flex;
	margin: 10vw;
}
</style>