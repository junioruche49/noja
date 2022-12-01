<template>
  <li :class="page.status == true ? 'active' : ''">
    <img :src="image" class="mr-2" /> {{ page.name }}
  </li>
</template>
<script>
export default {
  name: "NavBar",
  props: {
    page: Object,
  },
  data() {
    return {
      image: require(`../../assets/${this.page.icon}`),
    };
  },
};
</script>
<style scoped>
li {
  padding-bottom: 1.5rem;
  font-size: 0.9rem;
  font-weight: 500;
}
.active {
  color: #6868f7;
  font-weight: bold;
}
</style>