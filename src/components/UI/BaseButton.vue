<template>
  <button :class="[btnClass, 'btn']" :type="type">
    <slot></slot>
  </button>
</template>
<script>
export default {
  name: "BaseButton",
  props: {
    type: String,
    btnClass: String,
  },
};
</script>
<style>
.btn {
  border-radius: 5px;
  font-size: 0.9rem;
}
.primary {
  background: #f0f0fe;
  color: #6868f7;
  border: 0.5px solid #6868f7;
}
.secondary {
  background: rgba(235, 87, 87, 0.1);
  border: 0.5px solid #eb5757;
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