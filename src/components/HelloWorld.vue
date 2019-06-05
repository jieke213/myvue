<template>
  <div class="hello">
    {{msg}}
    <br>
    {{1>2 ? "是":"不是"}}

    <p class="ha">哈哈哈</p>
    <p v-bind:class="ha">呵呵呵</p>

    {{ ok ? "正确":"错误" }}<br>

    <template v-if="ok">
      <span>我是ok为true时显示的</span>
    </template>
    <template v-else="">
      <span>我是ok为false时显示的</span>
    </template>
    <br>

    <p v-show="flag">flag为true时显示</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '王景杰',
      ha: "哈",
      ok: false,
      flag: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
