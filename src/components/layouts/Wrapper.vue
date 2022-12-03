<template>
  <div class="container-fluid no-padding">
    <div class="row">
      <div class="col-2 full-height">
        <side-bar />
      </div>
      <div class="col-10 main-color">
        <main class="">
          <div class="container-fluid-2">
            <slot></slot>
          </div>
        </main>
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from "../sidebar/SideBar.vue";

export default {
  name: "Wrapper",
  components: { SideBar },
};
</script>
<style scoped>
.container-fluid-2 {
  width: 91%;
  margin: 0 auto;
}
.full-height {
  height: 100vh;
  padding-right: 0;
}
.main-color {
  background: #f5f6fd;
}
.no-padding {
  padding: 0;
}
</style>