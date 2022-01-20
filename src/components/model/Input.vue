<template>
  <div class="input">
    <input type="text" v-model="title" />
    <button @click="add">添加</button>
  </div>
</template>

<script>
import eventBus from '../js/event-bus';

export default {
  data() {
    return {
      title: ''
    }
  },
  methods: {
    add() {
      this.$emit('add', this.title);

      eventBus.$emit('addItem', this.title);
    }
  }
}
</script>

<style>

</style>
