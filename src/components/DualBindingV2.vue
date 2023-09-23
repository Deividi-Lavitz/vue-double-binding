<script setup lang="ts">
import { ref } from 'vue';

const textValue = ref('');
</script>

<template>
  <div>
    <input type="text" placeholder="Type your name" v-model="textValue" />
    <span>{{ textValue }}</span>
  </div>
</template>

<style scoped></style>
