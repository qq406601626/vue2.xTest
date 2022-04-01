<template>
  <div class="button">
    <span>button</span>
    <div v-if="loading" class="loading"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      loading: false
    }
  }
}
</script>

<style scoped lang="scss">
.button {
  width: 100px;
  height: 50px;
  background: dodgerblue;
  border-radius: 25px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
  font-size: 14px;

  .loading {
    width: 16px;
    height: 16px;
    border-radius: 50%;
    background: indianred;
  }
}
</style>
