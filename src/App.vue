<template>
  <div id="app">
    <!--<router-view></router-view>-->
    <div>app page</div>
    <div ref="box"></div>
  </div>
</template>
<script>

export default {
  data() {
    return {}
  },
  methods:{

  },
  mounted() {
    const data = {
      name:'zhangsan'
    }
    const v_object = {
      data(){
        return data
      },
      render(h) {
        return h('div',`name:${this.name}`)
      }
    }
    const v_node = this.$createElement(v_object)
    // 1、如果传第一个参数，则先把虚拟dom数据转换成真实dom，然后把生成的真实dom自动挂载到传入的节点中。
    // 2、如果不传第一个参数，则先把虚拟dom数据转换成真实dom，然后会生成一空dom节点，
    // 然后把生成的真实dom插入到前面生成的空dom节点中。然后返回该空dom节点。
    this.__patch__(this.$refs.box,v_node)
    setTimeout(()=>{
      data.name = 'lisi'
    },5000)
  }
}

</script>
<style lang="scss">
body {
  margin: 0;
  padding: 0;
}
</style>
