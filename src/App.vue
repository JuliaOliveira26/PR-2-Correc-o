<script setup>
import {livros} from '@/_data/livros.js'

</script>

<template>
  <h1>Minha Livraria</h1>
  <div class="listagem-livros">
    <h2>Livros disponíveis</h2>
    <div class="card-livro" v-for="livro in livros" :key="livro.id"></div>
    <img src="livro.img" alt="Capa do Livro" class="capa-livro">
    <div class="card-livro" v-for="livro in livros" :key="livro.id"> 
      <p class="titulo-livro">{{ livro.title }} </p>
      <p class=" autor-livro">{{ livro.author }}</p>
      <p class="preco-livro">{{ livro.rice }}</p>
    </div>
  </div>


</template>

<style scoped>
.listagem-livros{
  display: flex;
  flex-wrap: wrap;
}
.card-livro{
  margin: 5px 10px;
  padding: 10px;
  background-color: cornflowerblue;
  border-radius:  10px;
}

.capa-livro p{
  margin: 0;
}
.card-livro .titulo-livro{
  font-weight: bold;
  margin-bottom: 5px;
}
</style>
