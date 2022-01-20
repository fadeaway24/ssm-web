<template>
  <div class="comp-a">
    组件A
  </div>
</template>

<script>
export default {
  mounted() {
    console.log('组件A渲染');
  },
  destroyed() {
    console.log('组件A销毁')
  }
}
</script>

<style>

</style>