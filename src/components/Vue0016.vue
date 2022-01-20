<template>
  <div class="vue0016">
    <button @click="state = 'A'">A</button>
    <button @click="state = 'B'">B</button>
    <button @click="state = 'C'">C</button>

    <keep-alive>
      <comp-a v-if="state === 'A'"></comp-a>
      <comp-b v-if="state === 'B'"></comp-b>
      <comp-c v-if="state === 'C'"></comp-c>
    </keep-alive>

    <!-- <comp-a v-show="state === 'A'"></comp-a>
    <comp-b v-show="state === 'B'"></comp-b>
    <comp-c v-show="state === 'C'"></comp-c> -->
  </div>
</template>

<script>
import CompA from './model/CompA';
import CompB from './model/CompB';
import CompC from './model/CompC';
export default {
  data() {
    return {
      state: 'A',
    };
  },
  components: {
    CompA,
    CompB,
    CompC,
  },
};
</script>

<style></style>
