<script setup lang="ts">
import { ref } from 'vue';

const textValue = ref('');
const checkedState = ref(true);
const multiChecked = ref([]);
const selection = ref('');
//const selection = ref([]);
</script>

<template>
  <div>
    <input type="text" placeholder="Type your name" v-model.trim="textValue" />
    <span>{{ textValue }}</span>
  </div>
  <div>
    <input type="checkbox" v-model="checkedState" id="checkbox" />
    <label for="checkbox">{{ checkedState }}</label>
  </div>
  <div>
    <input
      type="checkbox"
      Value="Warrior"
      v-model="multiChecked"
      id="warrior"
    />
    <label for="warrior">Warrior</label>
    <input type="checkbox" Value="Mage" v-model="multiChecked" id="mage" />
    <label for="mage">Mage</label>
  </div>
  <div>{{ multiChecked }}</div>
  <div>
    <select v-model="selection">
      <option value="" disabled>Choose Wisely!</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
  </div>
</template>

<style scoped></style>
