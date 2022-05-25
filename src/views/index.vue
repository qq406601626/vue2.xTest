<template>
  <div class="container">
    <div>index container</div>

  </div>
</template>

<script>
import button from './button'

export default {
  extends: button,
  data() {
    return {
      loading: true
    };
  },
  methods: {},
  mounted() {
    console.log('2222222')
  }
};
</script>

<style lang="scss" scoped>
.container {
  width: 400px;
  height: 400px;
  background: gray;
}

</style>
