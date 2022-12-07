<template>
  <ul>
    <nav-bar v-for="page in pages" :page="page" :key="page.name" />
  </ul>
</template>
<script setup>
import NavBar from "./NavBar.vue";
import { defineProps, toRefs } from "vue";
const props = defineProps({
  pages: Array,
});

const { pages } = toRefs(props);
</script>
<style scoped>
ul {
  list-style: none;
  padding: 0;
}
</style>