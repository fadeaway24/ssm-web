<template>
  <div class="vue0013">
    <layout>
      <template v-slot:header>
        <h1>标题</h1>
      </template>

      <p>主体内容1</p>
      <p>主体内容2</p>

      <template v-slot:footer>
        <p>联系方式</p>
      </template>
    </layout>

    <hr>

    <my-menu>
      <template
        v-for="item in menuData"
      >
        <!-- 判断有无子菜单 -->
        <!-- 无子菜单的菜单项 开始 -->
        <menu-item v-if="!item.children" :key="item.id">
          {{ item.title }}
        </menu-item>
        <!-- 无子菜单的菜单项 结束 -->

        <!-- 有子菜单的菜单项 开始 -->
        <sub-menu-item v-else :key="item.id">
          <!-- 通过名字为 title 的 slot 传入菜单项标题 -->
          <template v-slot:title>
            {{ item.title }}
          </template>

          <!-- 通过名字为 content 的 slot 传入子菜单的内容 -->
          <template v-slot:content>
            <!-- 子菜单循环 开始 -->
            <menu-item
              v-for="child in item.children"
              :key="child.id"
            >
              {{ child.title }}
            </menu-item>
            <!-- 子菜单循环 结束 -->
          </template>
        </sub-menu-item>
        <!-- 有子菜单的菜单项 结束 -->
      </template>
    </my-menu>

  </div>
</template>

<script>
import menuData from './mockdata/menuData';

import Layout from './model/Layout';
import MyMenu from './model/Menu';
import MenuItem from './model/MenuItem';
import SubMenuItem from './model/SubMenuItem';

export default {
  data() {
    return {
      menuData
    }
  },
  components: {
    Layout,
    MyMenu,
    MenuItem,
    SubMenuItem
  },
};
</script>

<style></style>
