<template>
  <div>
    hello
    <Children :html="result" />
  </div>
</template>
<script setup lang="ts">
import Children from "./components/Children.vue";

const result = ref("");
const { data } = await useAsyncData("item", () =>
  $fetch("http://localhost:3001")
);

watch(
  data,
  () => {
    result.value = data.value;
  },
  { immediate: true }
);
</script>