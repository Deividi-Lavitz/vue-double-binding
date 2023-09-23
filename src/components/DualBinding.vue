<script setup lang="ts">
function inputHandle(event: Event) {
  const textBox = event.currentTarget as HTMLInputElement;
  console.log(textBox.valeu);
}
</script>

<template>
  <div>
    <input type="text" placeholde="Type your name" @input="inputHandle" />
    <span></span>
  </div>
</template>

<style scoped></style>
