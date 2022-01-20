<template>
  <div id="app">
    <comp-e></comp-e>
    <hr>
    <comp-f></comp-f>
  </div>
</template>

<script>
import CompE from './model/CompE';
import CompF from './model/CompF';

export default {
  components: {
    CompE,
    CompF
  }
}
</script>

<style>

</style>
