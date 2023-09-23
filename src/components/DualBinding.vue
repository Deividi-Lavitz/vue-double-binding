<script setup lang="ts">
import { ref } from 'vue';

const textValue = ref('');

function inputHandle(event: Event) {
  const textBox = event.currentTarget as HTMLInputElement;
  textValue.value = textBox.value;
}
</script>

<template>
  <div>
    <input
      type="text"
      placeholder="Type your name"
      @input="inputHandle"
      :value="textValue"
    />
    <span>{{ textValue }}</span>
  </div>
</template>

<style scoped></style>
