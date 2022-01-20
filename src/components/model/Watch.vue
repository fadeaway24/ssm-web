<template>
  <div class="watch">
    <input type="text" v-model="name" />
    <p>{{ name }}</p>
    <input type="text" v-model="info.hobby" />
    <p>{{ info }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '哈默',
      info: {
        hobby: '篮球',
      },
    };
  },
  watch: {
    name(newValue, oldValue) {
      console.log('name', newValue, oldValue);
    },
    // info(newValue, oldValue) {
    //   console.log('info', newValue, oldValue);
    // },
    info: {
      handler: function (newValue, oldValue) {
        console.log('info', newValue, oldValue);
      },
      // 深度监听
      deep: true
    },
  },
};
</script>

<style></style>
