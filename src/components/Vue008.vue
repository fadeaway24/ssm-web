<template>
  <div class="vue008">
    <MyInput @add="add" />
    <MyList :list="list" />
  </div>
</template>

<script>
import MyInput from './model/Input';
import MyList from './model/List';

export default {
  data() {
    return {
      list: [
        {
          id: 1,
          title: '标题1'
        },
        {
          id: 2,
          title: '标题2'
        }
      ]
    }
  },
  methods: {
    add(title) {
      this.list.push({
        id: Math.random(),
        title
      })
    }
  },
  components: {
    MyInput,
    MyList
  }
}
</script>

<style>

</style>
