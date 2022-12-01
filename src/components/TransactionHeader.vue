<template>
  <div class="row trans-header-bg-white">
    <div class="col-12 no-padding">
      <base-button class="primary mr-3">Add Income</base-button>
      <base-button class="secondary mr-3">Add Expense</base-button>
      <base-button class="tertiary">View Debts</base-button>
    </div>
  </div>
</template>
<script>
import BaseButton from "./UI/BaseButton.vue";
export default {
  components: { BaseButton },
  name: "TransactionHeader",
};
</script>
<style>
.trans-header-bg-white {
  background-color: #fff;
  padding: 1.5rem 1rem;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}
.no-padding {
  padding-left: 0;
}
</style>