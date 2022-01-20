<template>
  <div class="comp-b">
    组件B
  </div>
</template>

<script>
export default {
  mounted() {
    console.log('组件B渲染');
  },
  destroyed() {
    console.log('组件B销毁')
  }
}
</script>

<style>

</style>