<template>
  <div class="vue009">
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
  created() {
    console.log('parent: App created');
  },
  mounted() {
    console.log('parent: App mounted');
  },
  beforeUpdate() {
    console.log('parent: App before update');
  },
  updated() {
    console.log('parent: App updated');
  },
  components: {
    MyInput,
    MyList
  }
}
</script>

<style>

</style>
