<template>
    <div>
        <section class="books-section">
            <h2>Top 10 Best sellers books in Spain 2024</h2>
            <div v-if="pending">Loading...</div>
            <div v-else-if="error">Error: {{ error.message }}</div>
            <button class="button-link">
                <NuxtLink to="/">Back home</NuxtLink>
            </button>
        </section>
        <section class="bookcard-section">
            <BookCard v-for="book in books" :key="book.id" :book="book" />
        </section>
    </div>
</template>

<script setup>

const { data: books, pending, error } = await useAsyncData('books', () => 
  $fetch(`http://127.0.0.1:8000/api/books/`)
)

</script>

<style lang="scss">
@import '~/assets/scss/books-list.scss';
</style>