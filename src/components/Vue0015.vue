<template>
  <div class="vue0015">
    <test v-if="show"></test>
    <button @click="show = true">显示 Test 组件</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false
    }
  },
  components: {
    Test: () => import(/* webpackChunkName: "test" */ './model/Test')
  }
}
</script>

<style>

</style>
