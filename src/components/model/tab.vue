<template>
  <div class="tab" @click="handleClick">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    value: String
  },
  methods: {
    handleClick() {
      this.$parent.trigger(this.value);
    }
  }
}
</script>

<style>
.tab {
  flex: 1;
  padding: 10px 0;
  text-align: center;
  color: #fff;
  cursor: pointer;
}
</style>