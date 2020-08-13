<template>
  <div id="app">
    <myMain/>
    <myFoot/>
  </div>
</template>

<script>
import myMain from '@/components/searchbar.vue'
import myFoot from '@/components/foot.vue'

export default {
  name: 'App',
  components: {
    myMain,
    myFoot
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
body{
  background-image: url(assets/bg.png);
  background-repeat: no repeat;
  background-size: cover;
  margin: 0px;
}
</style>
