<template>
  <div class="page-con">
    <Header />
    <div class="view-con">
      <router-view />
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #6e4a90;
}
body{
  margin: 0px;
  padding: 0px;
}
.page-con {
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  background-color: rgb(225, 227, 241);
}
.view-con {
  flex-grow: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
