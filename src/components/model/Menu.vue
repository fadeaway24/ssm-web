<template>
  <ul class="menu">
    <slot></slot>
  </ul>
</template>

<script>
export default {
  name: 'Menu'
}
</script>

<style>
.menu {
  width: 300px;
  background-color: #000;
}
</style>