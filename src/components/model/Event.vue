<template>
  <div id="event">
    <p>{{ number }}</p>
    <button @click="incrementBy1">点击加1</button>
    <button @click="incrementBy10(10, $event)">点击加10</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0
    }
  },
  methods: {
    incrementBy1(e) {
      this.number++;
      console.log('e', e);
      console.log(e.__proto__.constructor);
      console.log('e.target', e.target);
      console.log('e.currentTarget', e.currentTarget);
    },
    incrementBy10(step, e) {
      this.number += step;
      console.log('e', e);
    }
  }
}
</script>

<style>

</style>