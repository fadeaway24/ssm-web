<template>
  <div class="comp-e">
    <p>{{ aData }}</p>
    <p>{{ commonData }}</p>
    <button @click="aMethod">eMethod</button>
    <button @click="commonMethod">commonMethod</button>
  </div>
</template>

<script>
import mixin from '../mixins/mixin';

export default {
  mixins: [mixin],
  data() {
    return {
      aData: '组件A的数据'
    }
  },
  methods: {
    aMethod() {
      console.log('组件E的方法');
    }
  },
  mounted() {
    console.log('组件E mounted');
  }
}
</script>

<style>

</style>
