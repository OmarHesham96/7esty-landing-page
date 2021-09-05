<script>
import heads from './components/heads.vue'
import countDown from './components/countDown.vue'

export default {
  name: 'app',
  components: {
    heads,
    countDown
  },
}
</script>

<template>
  <heads />
  <countDown />
</template>

<style>
#app {
  background: url("../src/assets/bg.png") no-repeat center fixed;
  background-size: cover;
  background-position-y: -12%;
  height:45em;
}
</style>
