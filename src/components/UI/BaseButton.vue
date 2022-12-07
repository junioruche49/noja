<template>
  <button :class="[props.btnClass, 'btn-2']" :type="props.type">
    <slot></slot>
  </button>
</template>
<script setup lang="ts">
import { defineProps } from "vue";
const props = defineProps({
  type: String,
  btnClass: String,
});
</script>
<style>
.btn-2 {
  border-radius: 5px;
  font-size: 0.9rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 13px;
  padding-top: 0;
  padding-bottom: 0;
}
.primary {
  background: #f0f0fe;
  color: #6868f7;
  border: 1px solid #6868f7;
}
.secondary {
  background: rgba(235, 87, 87, 0.1);
  border: 1px solid #eb5757;
  color: #eb5757;
}
.tertiary {
  background: #f2f2f2;
  border: 1px solid #bdbbc9;
}
.btn-icon {
  background: transparent;
  border: 1px solid #bdbbc9;
  padding: 3px 6px;
}
</style>