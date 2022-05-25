<template>
  <div id="app">
    <router-view></router-view>
    <div ref="box"></div>
  </div>
</template>
<script>

export default {
  data() {
    return {}
  },
  methods:{ },
  mounted() {
    const h1 = this.$createElement('h1','1111111111')
    console.log('xxxxx')
    const dom = this.__patch__(null,h1)
    document.body.appendChild(dom)
  }
}

</script>
<style lang="scss">
body {
  margin: 0;
  padding: 0;
}
</style>
