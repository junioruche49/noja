<template>
  <li>
    <router-link to="/" :class="page.status == true ? 'active' : ''">
      <img :src="image" class="mr-2" /> {{ page.name }}
    </router-link>
  </li>
</template>
<script setup>
import { defineProps, toRefs } from "vue";
const props = defineProps({
  page: Object,
});
const { page } = toRefs(props);
const image = require(`../../assets/${page.value.icon}`);
</script>
<style scoped>
li {
  padding-bottom: 1.5rem;
  font-size: 0.9rem;
  font-weight: 500;
}
a {
  color: black;
}
a:hover {
  text-decoration: none;
}
.active,
a:active,
a.router-link-active {
  color: #6868f7;
  font-weight: bold;
}
</style>