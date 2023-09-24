<script setup lang="ts">
import { ref, computed } from 'vue';

const autor = ref({
  id: 1,
  name: 'Lavitz',
  books: [],
});

const message = computed(() => {
  return autor.value.books.lenght > 0 ? 'Lots of Books' : 'No Books';
});
</script>

<template>
  <h1>{{ autor.name }}</h1>
  <h2>Books:</h2>
  <span>{{ message }}</span>
</template>

<style scoped></style>
