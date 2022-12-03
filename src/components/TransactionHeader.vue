<template>
  <div class="row trans-header-bg-white">
    <div class="col-12 no-padding">
      <div class="form-row">
        <base-button class="primary mr-3"
          ><img src="../assets/plus.svg" class="img-btn mr-2 ml-1" /> Add
          Income</base-button
        >
        <base-button class="secondary mr-3" @click="$emit('toggle-expense')"
          ><img src="../assets/plus-2.svg" class="img-btn mr-2 ml-1" /> Add
          Expense</base-button
        >
        <base-button class="tertiary mr-3">View Debts</base-button>
        <input
          type="text"
          class="form-control form-width-7 mr-3"
          placeholder="Search transactions"
        />
        <base-button class="tertiary">
          <img src="../assets/ic-filter.svg" class="img-btn mr-2 ml-1" />
          Filter</base-button
        >
      </div>
    </div>
  </div>
</template>
<script>
import BaseButton from "./UI/BaseButton.vue";
export default {
  components: { BaseButton },
  name: "TransactionHeader",
  emits: ["toggle-expense"],
  methods: {
    clickIt() {
      console.log("erere");
    },
  },
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
.form-width-7 {
  width: 59%;
}
.img-btn {
  width: 16px;
}
</style>