<template>
  <div class="computed">
    <p>{{ number }}</p>
    <p>double1: {{ double1 }}</p>
    <input v-model="double2" />
    {{ double2 }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 5,
      testNum: 100
    }
  },
  computed: {
    // double1() {
    //   console.log('double1 运行了');
    //   return this.number * 2;
    // },
    double1: {
      get() {
        return this.number * 2;
      }
    },
    // double2() {
    //   return this.number * 2;
    // }
    double2: {
      get() {
        return this.number * 2;
      },
      set(value) {
        this.number = value / 2;
      }
    }
  }
}
</script>

<style></style>
