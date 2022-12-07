<template>
  <li>
    <router-link to="/" :class="props.page.status == true ? 'active' : ''">
      <img :src="image" class="mr-2" /> {{ props.page.name }}
    </router-link>
  </li>
</template>
<script setup lang="ts">
import { defineProps } from "vue";
const props = defineProps({
  page: Object,
});
const image = require(`../../assets/${props.page.icon}`);
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