<template>
  <!-- <ul class="list clearfix">
    <li class="item active">项目1</li>
    <li class="item">项目2</li>
    <li class="item">项目3</li>
  </ul> -->
  <!-- <ul class="list clearfix">
    <li class="item" :class="{'active': isActive}">项目1</li>
    <li class="item">项目2</li>
    <li class="item">项目3</li>
  </ul> -->
  <!-- <ul class="list clearfix">
    <li class="item" :class="['active']">项目1</li>
    <li class="item">项目2</li>
    <li class="item">项目3</li>
  </ul> -->
  <ul class="list clearfix">
    <li class="item" :style="styleData">项目1</li>
    <li class="item">项目2</li>
    <li class="item">项目3</li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
      styleData: {
        backgroundColor: '#424242',
        color: '#ffffff'
      }
    }
  }
}
</script>

<style>
ul {
  padding: 0;
  margin: 0;
  list-style: none;
}

.clearfix:after {
  display: block;
  content: '';
  clear: both;
}

.list {
  width: 300px;
  border: 5px solid #424242;
}

.item {
  float: left;
  width: 100px;
  height: 50px;
  text-align: center;
  line-height: 50px;
  font-weight: 700;
}
.active {
  background-color: #424242;
  color: #fff;
}
</style>