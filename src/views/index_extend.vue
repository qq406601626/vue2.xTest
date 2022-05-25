<template>
  <div class="container">
    <button @click="appendButton">appendButton</button>
  </div>
</template>

<script>
import Vue from 'vue'
import button from './button'

export default {
  data() {
    return {};
  },
  methods: {
    appendButton() {
      const Button = Vue.extend(button)
      const buttonInstance = new Button()
      const buttonEl = buttonInstance.$mount()
      this.$el.appendChild(buttonEl.$el)
      setTimeout(() => {
        buttonInstance.loading = true
      }, 2000)
    }
  },
};
</script>

<style lang="scss" scoped>
.container {
  width: 400px;
  height: 400px;
  background: gray;
}

</style>
