<template>
  <div class="tab-bar">
    <tab 
      v-for="(item, index) in data"
      :key="index"
      :value="item.label"
    >
      {{ item.label }}
    </tab>
  </div>
</template>

<script>
import Tab from './tab';

export default {
  props: {
    data: Array
  },
  methods: {
    trigger(value) {
      this.$emit('input', value);
    }
  },
  components: {
    Tab
  }
}
</script>

<style>
.tab-bar {
  width: 300px;
  display: flex;
  background-color: #424242;
}
</style>