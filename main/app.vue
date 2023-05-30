<template>
  <div>
    hello
    <Children :html="result" />
  </div>
</template>
<script setup lang="ts">
import Children from "./components/Children.vue";

const result = ref("");

async function fetchChildren() {
  result.value = await $fetch("http://localhost:3000");
}

fetchChildren();
</script>