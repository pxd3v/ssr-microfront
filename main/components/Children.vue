<template>
  <div v-html="html"></div>
</template>

<script setup lang="ts">
type Props = {
  html: string;
};

const props = defineProps<Props>();
</script>