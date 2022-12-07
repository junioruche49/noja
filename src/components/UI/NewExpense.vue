<template>
  <teleport to="body">
    <div class="bg-cover">
      <dialog open>
        <div class="row">
          <div class="col-6">
            <h6>New Expense</h6>
          </div>
          <div class="col-6 text-right">
            <base-button @click="emits('toggle-expense')"
              ><img src="../../assets/x.svg" class="img-btn" />
            </base-button>
          </div>
        </div>
        <form>
          <div class="form-group">
            <label for="AmountSpent">Amount Spent</label>
            <input
              type="number"
              class="form-control"
              id="AmountSpent"
              placeholder="₦0.00"
            />
          </div>
          <div class="form-row">
            <div class="form-group col-md-6">
              <label for="paymentMethod">Payment Method</label>
              <select class="custom-select" id="paymentMethod" required>
                <option>Cash</option>
                <option>Bank Transfer</option>
                <option>Card</option>
              </select>
            </div>
            <div class="form-group col-md-6">
              <label for="expenseDate">Date of Expense</label>
              <input type="date" class="form-control" id="expenseDate" />
            </div>
          </div>
          <div class="form-group">
            <label for="paymentDetails"
              >What was this payment for? (optional)</label
            >
            <textarea
              class="form-control"
              id="paymentDetails"
              rows="3"
            ></textarea>
          </div>
          <div class="form-row">
            <div class="form-group col-md-6">
              <div class="custom-control custom-checkbox my-1 mr-sm-2">
                <input
                  type="checkbox"
                  class="custom-control-input"
                  id="customControlInline"
                />
                <label class="custom-control-label" for="customControlInline"
                  >Create new after submiting</label
                >
              </div>
            </div>
            <div class="form-group col-md-6">
              <button class="btn btn-primary btn-block btn-full" type="submit">
                Save Expense
              </button>
            </div>
          </div>
        </form>
      </dialog>
    </div>
  </teleport>
</template>
<script setup lang="ts">
import { defineEmits } from "vue";
const emits = defineEmits(["toggle-expense"]);
</script>

<style scoped>
.bg-cover {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.75);
  z-index: 10;
}

dialog {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 35%;
  z-index: 100;
  border-radius: 12px;
  border: none;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 20px;
  margin: 0;
  overflow: hidden;
}
.btn-full {
  background-color: #6868f7;
}
</style>