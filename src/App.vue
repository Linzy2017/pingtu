<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
#app{
  position: absolute;
  width: 100%;
  min-height: 100%;
  background: url("./assets/bg.png");
  background-size: 100%;
}
</style>
