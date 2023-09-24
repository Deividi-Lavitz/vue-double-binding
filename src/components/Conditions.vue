<script setup lang="ts">
import { ref } from 'vue';

const itsOn = ref(true);
const weapons = ref([
  { name: 'Shotgun', ammo: '12 gauge', status: true },
  { name: 'Pistol', ammo: '9mm', status: false },
  { name: 'Rocket Launcher', ammo: 'Rockets', status: false },
]);
</script>

<template>
  <div>
    <button type="button" @click="itsOn = !itsOn">Click!</button>
    <span>{{ itsOn }}</span>
    <h1 v-if="itsOn">Hello Stranger</h1>
    <h1 v-else="itsOn">Come Back anytime</h1>
  </div>
  <template v-if="itsOn">
    <div>
      <h2>Gotta a nice selection of good things for yah!</h2>
      <ul>
        <li v-for="weapon in weapons">
          {{ weapon.name }}
        </li>
        <li v-for="(weapon, index) in weapons" :key="index">
          {{ index }} - {{ weapon.ammo }}
        </li>
      </ul>
    </div>
  </template>
  <template v-if="!itsOn" v-for="weapon in weapons">
    <ul>
      <li v-if="weapon.status">
        {{ weapon.name }}
      </li>
    </ul>
  </template>
</template>

<style></style>
