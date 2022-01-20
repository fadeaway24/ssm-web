<template>
  <div class="comp-f">
    <p>{{ bData }}</p>
    <p>{{ commonData }}</p>
    <button @click="bMethod">fMethod</button>
    <button @click="commonMethod">commonMethod</button>
  </div>
</template>

<script>
import mixin from '../mixins/mixin';

export default {
  mixins: [mixin],
  data() {
    return {
      bData: '组件F的数据'
    }
  },
  methods: {
    bMethod() {
      console.log('组件F的方法');
    }
  },
  mounted() {
    console.log('组件B mounted');
  }
}
</script>

<style>

</style>
