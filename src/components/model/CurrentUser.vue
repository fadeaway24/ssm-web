<template>
  <h1>
    <slot :user="user">
      {{ user.name }}
    </slot>
  </h1>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: '哈默',
        age: 20
      }
    }
  }
}
</script>

<style>

</style>