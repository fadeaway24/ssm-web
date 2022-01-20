<template>
  <div class="vue0018">
    <input type="text" v-model="message">
    <h1>meesage: {{ message }}</h1>

    <hr>

    <tab-bar
      :data="tabs"
      v-model="selectedLabel"
    >
    </tab-bar>

    <h1>当前选项：{{ selectedLabel }}</h1>
  </div>
</template>

<script>
import TabBar from './model/tab-bar';

export default {
  data() {
    return {
      message: '我是哈默',
      index: 0,
      tabs: [
        { label: '选项1' },
        { label: '选项2' },
        { label: '选项3' }
      ],
    };
  },
  computed: {
    // selectedLabel() {
    //   return this.tabs[this.index].label;
    // }
    // this.selectedLabel = xxx;
    selectedLabel: {
      get() {
        return this.tabs[this.index].label;
      },
      set(newVal) {
        this.index = this.tabs.findIndex(tab => {
          return tab.label === newVal;
        })
      }
    }
  },
  components: {
    TabBar
  }
};
</script>

<style></style>
