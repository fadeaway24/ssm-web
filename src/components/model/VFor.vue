<template>
  <div class="vfor">
    <h1>遍历数组</h1>
    <ul >
      <li  v-for="(item, index) in array" :key="item.id">
        <span v-if="flag">xxx</span>
        {{ index }} - {{ item.value }}
      </li>
    </ul>

    <hr>

    <h1>遍历对象</h1>
    <ul>
      <li v-for="(value, key, index) in object" :key="key">
        {{ index }} - {{ key }} - {{ value }}
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  data() {
    return {
      flag: false,
      array: [
        { id: 1, value: '项目1' },
        { id: 2, value: '项目2' },
        { id: 3, value: '项目3' }
      ],
      object: {
        name: '哈默',
        hobby: '篮球'
      }
    }
  }
}
</script>

<style>

</style>