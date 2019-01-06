<template>
  <div id="app">
    <headerNav></headerNav>
    <div class="content-wrap">
      <leftNav></leftNav>
      <breadcrumb></breadcrumb>
      <div class="main-wrap">
        <router-view />
      </div>
    </div>
  </div>
</template>

<script>
import headerNav from './components/header-nav/header-nav.vue'
import leftNav from './components/left-nav/left-nav.vue'
import breadcrumb from './components/breadcrumb/breadcrumb.vue'

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    headerNav,
    leftNav,
    breadcrumb,
  },
}
</script>

<style lang="less">
body {
  overflow-x: hidden
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow-x: hidden;
  .content-wrap {
    width: 100%;
    position: absolute; 
    margin-top: 0px;
    .main-wrap {
      float:left; 
      width: calc(100% - 195px); 
      margin-left: 160px; 
      position: relative;
      top: 30px; 
    }
  }
}


</style>
