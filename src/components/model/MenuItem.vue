<template>
  <li class="menu-item">
    <slot></slot>
  </li>
</template>

<script>
export default {
  name: 'MenuItem'
}
</script>

<style>
.menu-item {
  height: 50px;
  line-height: 50px;
  text-align: center;
  color: #fff;
}
</style>