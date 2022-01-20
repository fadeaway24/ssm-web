<template>
  <div class="vue001">
    {{ name }}

    <p id="test">{{ name }}</p>
    <p :id="dynamicId">{{ name }}</p>

    <p>{{ number }}</p>
    <p>{{ number + 1 }}</p>
    <p>{{ flag ? 'Yes': 'No'}}</p>
    <p>{{ name.split('').reverse().join('') }}</p>

    <!-- <p>{{ var a = 1 }}</p>
    <p>{{ if(flag) { return 'Hello' } }}</p> -->

    <div v-html="html1"></div>

    <div v-html="html2">
      <p>我是哈默</p>
    </div>

    <div v-html="html3"></div>
  </div>
</template>

<script>
export default {
  name: 'Vue001',
  data() {
    return {
      name: '哈默',
      dynamicId: Math.random(),
      number: 1,
      flag: true,
      html1: '<p>我是哈默</p>',
      html2: '<h1>我是哈默</h1>',
      html3: `<img src="123" onerror="alert('Hey! 我是黑客哈默~~~~（开玩笑的）')" />`
    }
  }
}
</script>

<style>

</style>
