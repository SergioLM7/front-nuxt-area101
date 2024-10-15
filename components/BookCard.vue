<template>
    <div class="book-card">
      <img :src="book.imagen" :alt="book.titulo" class="book-image">
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