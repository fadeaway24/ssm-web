<template>
  <li class="menu-item">
    <div class="title">
      <!-- 名字为 title 的插槽，负责 插入标题 -->
      <slot name="title"></slot>
      <span class="icon">&gt;</span>
    </div>
    <ul class="content">
      <!-- 名字为 content 的插槽，负责 插入子菜单内容 -->
      <slot name="content"></slot>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'SubMenuItem'
}
</script>

<style>
.menu-item {
  position: relative;
}

.menu-item .icon {
  position: absolute;
  top: 0;
  right: 15px;
}

.menu-item .content {
  position: absolute;
  top: 0;
  left: 100%;
  width: 100%;
  background-color: #424242;
}
</style>