<template>
  <nav class="sidebar pt-5 pl-3 pr-3">
    <div class="row mb-4">
      <div class="col-6">
        <img src="../../assets/Noja360-Logo-transparent.svg" alt="" srcset="" />
      </div>
      <div class="col-6 text-right">
        <base-button btnClass="btn-icon">
          <img src="../../assets/menu.png" alt="" srcset="" />
        </base-button>
      </div>
    </div>
    <nav-bars :pages="pages" />
  </nav>
</template>
<script>
import BaseButton from "../UI/BaseButton.vue";
import NavBars from "../UI/NavBars.vue";
export default {
  components: { NavBars, BaseButton },
  data() {
    return {
      pages: [
        {
          name: "Dashboard",
          status: false,
          icon: "menu-icon.svg",
        },
        {
          name: "Customers",
          status: false,
          icon: "users.svg",
        },
        {
          name: "Products",
          status: false,
          icon: "package.svg",
        },
        {
          name: "Transactions",
          status: true,
          icon: "file-minus.svg",
        },
        {
          name: "Discounts",
          status: false,
          icon: "Frame.svg",
        },
        {
          name: "Customers Groups",
          status: false,
          icon: "users.svg",
        },
        {
          name: "Invoices",
          status: false,
          icon: "file-minus-1.svg",
        },
        {
          name: "Sales Targets",
          status: false,
          icon: "target.svg",
        },
      ],
    };
  },
};
</script>
<style scoped>
nav {
  background-color: #f9fafc;
  border-right: 0.5px solid #ccc;
  height: 100%;
}
</style>