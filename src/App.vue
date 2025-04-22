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
</script>

<template>
  <header>
      <h1>IFbooks</h1>
        <p>
          <span>| Apreço a leiitura</span>
        </p>
      <div class="search">
        <input type="text" v-model="search" placeholder="Pesquisar" class="barra">
        <ul>
      <li
        v-for="item in filteredItems"
        :key="item"
        class="filtro"
      >
        {{ item }}
      </li>
    </ul>
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
  </ul>
  <div class="icons">
    <ul>
      <li>
        <i class="fas fa-shopping-cart"></i>
      </li>
      <li>
        <i class="fa-solid fa-heart"></i>
      </li>
      <li>
        <i class="fa-solid fa-user"></i>
      </li>
    </ul>
  </div>
  </header>

  <main>
    <section>
      <div>
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
      </ul>
    </section>
    <section>
      <h2>
        Lançamentos
      </h2>
      <div>
        <img src="/public/imagens/97819821858242.png" alt="">
        <h3>Chain of Iron: Volume 2</h3>
        <p>Cassandra Clare</p>
        <p>R$ {{ valorLivro1 }}</p>
      </div>
    </section>
  </main>
</template>

<style scoped>
</style>