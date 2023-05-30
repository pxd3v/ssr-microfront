<template>
  <div>
    <button @click="onClick">Click here to increase value</button>
    <h1>Value: {{ value }}</h1>
  </div>
</template>

<script setup lang="ts">
const value = ref(0);
function onClick() {
  value.value += 1;
}
</script>