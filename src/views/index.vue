<template>
  <div>
    <el-button @click="setPage1">setPage1</el-button>
    <el-button @click="setPage2">setPage2</el-button>
    <el-button @click="setPage3">setPage3</el-button>
    <el-table :data="list" border row-key="id" @selection-change="selectionChange">
      <el-table-column type="selection" reserve-selection></el-table-column>
      <el-table-column prop="label" label="label"></el-table-column>
    </el-table>
  </div>
</template>

<script>

export default {
  data() {
    return {
      source: [
        {id: 1, label: 1},
        {id: 2, label: 2},
        {id: 3, label: 3},
        {id: 4, label: 4},
        {id: 5, label: 5},
        {id: 6, label: 6},
        {id: 7, label: 7},
        {id: 8, label: 8},
        {id: 9, label: 9},
        {id: 10, label: 10},
      ],
      list: []
    };
  },
  methods: {
    setPage1() {
      this.list = this.source.slice(0, 3)
    },
    setPage2() {
      this.list = this.source.slice(3, 6)

    },
    setPage3() {
      this.list = this.source.slice(6, 9)
    },
    selectionChange(rows){
      console.log(rows)
    }
  },

};
</script>

<style lang="scss" scoped>


</style>
