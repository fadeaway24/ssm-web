<template>
  <div class="list">
    <ul>
      <li v-for="item in list" :key="item.id">
        {{ item.title }}
      </li>
    </ul>
  </div>
</template>

<script>
import eventBus from '../js/event-bus';

export default {
  props: {
    list: Array
  },
  methods: {
    handleAddTitle(title) {
      console.log('title', title);
    }
  },
  created() {
    console.log('child: List created');
  },
  mounted() {
    console.log('child: List mounted');
    eventBus.$on('addItem', this.handleAddTitle);
  },
  beforeUpdate() {
    console.log('child: List before update');
  },
  updated() {
    console.log('child: List updated');
  },
  beforeDestroy() {
    eventBus.$off('addItem', this.handleAddTitle);
  }
}
</script>

<style>

</style>
