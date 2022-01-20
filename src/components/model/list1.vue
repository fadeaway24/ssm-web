<template>
  <ul class="list1">
    <item
      v-for="(item, index) in listData"
      :key="index"
      :text="item"
    >
    </item>
  </ul>
</template>

<script>
import item from './item';

export default {
  props: ['listData'],
  components: {
    item
  }
}
</script>

<style>

</style>
