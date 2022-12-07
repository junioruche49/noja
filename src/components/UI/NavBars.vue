<template>
  <ul>
    <nav-bar v-for="page in pages.pages" :page="page" :key="page.name" />
  </ul>
</template>
<script setup lang="ts">
import NavBar from "./NavBar.vue";
import { defineProps } from "vue";
const pages = defineProps({
  pages: Array,
});
</script>
<style scoped>
ul {
  list-style: none;
  padding: 0;
}
</style>