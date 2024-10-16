<template>
    <div class="book-card">
      <a :href="book.url" target="_blank" rel="noopener noreferrer">
        <img :src="book.imagen" :alt="book.titulo" class="book-image" >
      </a>
      <h2>{{ book.titulo }}</h2>
      <p>{{ book.autor }}</p>
      <i>{{ book.precio }}€</i>
    </div>
</template>
<script setup>
  defineProps(['book']);
</script>
<style>
    @import '~/assets/scss/bookcard.scss';
</style>