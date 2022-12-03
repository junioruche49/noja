<template>
  <wrapper>
    <div class="row pt-5 mb-3">
      <h3 class="trans-header">Transactions (56)</h3>
    </div>
    <transaction-header @toggle-expense="toggleForm" />
    <Transaction-table />
    <new-expense @toggle-expense="toggleForm" v-if="newExpenseForm" />
  </wrapper>
</template>
<script>
import Wrapper from "../components/layouts/Wrapper.vue";
import TransactionHeader from "../components/TransactionHeader.vue";
import { ref } from "vue";
import NewExpense from "@/components/UI/NewExpense.vue";
import TransactionTable from "@/components/TransactionTable.vue";

export default {
  name: "TransactionList",
  components: { Wrapper, TransactionHeader, NewExpense, TransactionTable },
  setup() {
    let newExpenseForm = ref(false);

    function toggleNewExpenseForm() {
      newExpenseForm.value = !newExpenseForm.value;
    }

    return { toggleForm: toggleNewExpenseForm, newExpenseForm };
  },
};
</script>
<style>
.trans-header {
  font-size: 1.2rem;
  color: #5a5477;
}
</style>
