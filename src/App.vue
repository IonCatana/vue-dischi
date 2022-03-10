<template>
  <div id="app">
    <MyHeader />
    <MyMain />
    <MusicList />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import MusicList from './components/MusicList.vue'
export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MusicList,
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
img{
  width: 100%;
}
#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
}
</style>
