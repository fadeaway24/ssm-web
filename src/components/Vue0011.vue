<template>
  <div class="vue0011">
    <slot-test>
      <p>我是哈默</p>
    </slot-test>

    <hr>

    <list1 :listData="listData"></list1>

    <hr>

    <list-slot>
      <item-slot>Vue - 使用插槽 - 项目1</item-slot>
      <item-slot>Vue - 使用插槽 - 项目2</item-slot>
      <item-slot>Vue - 使用插槽 - 项目3</item-slot>
    </list-slot>

    <hr>

    <ul>
      <li>原生HTML - 项目1</li>
      <li>原生HTML - 项目2</li>
      <li>原生HTML - 项目3</li>
    </ul>
  </div>
</template>

<script>
import slotTest from './model/slotTest';
import list1 from './model/list1';
import listSlot from './model/listSlot';
import itemSlot from './model/itemSlot';

export default {
  data() {
    return {
      listData: [
        'Vue - 不使用插槽 - 项目1',
        'Vue - 不使用插槽 - 项目2',
        'Vue - 不使用插槽 - 项目3'
      ]
    }
  },
  components: {
    slotTest,
    list1,
    listSlot,
    itemSlot
  }
}
</script>

<style>

</style>
