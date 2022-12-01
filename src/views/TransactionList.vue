<template>
  <wrapper>
    <div class="row pt-5 mb-3">
      <h3 class="trans-header">Transactions</h3>
    </div>
    <transaction-header />
  </wrapper>
</template>
<script>
import Wrapper from "../components/layouts/Wrapper.vue";
import TransactionHeader from "../components/TransactionHeader.vue";

export default {
  name: "TransactionList",
  components: { Wrapper, TransactionHeader },
};
</script>
<style>
.trans-header {
  font-size: 1.2rem;
}
</style>
