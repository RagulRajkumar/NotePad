<template>
  <div id="app">
    <div class="nabarx">
      <h1>NotePad</h1>
    </div>
    <Header/>
    <h1 class="footer"> Developed By <a href="https://www.linkedin.com/in/ragul-rajkumar-4b7246195/" target="_blank">Ragul Rajkumar</a></h1>
  </div>
</template>

<script>
import Header from './components/Header.vue'
export default {
  name: 'App',
  components: {
    Header
  },
  methods:{
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
}
.nabarx{
  background-color: #2c3e50;
  margin-bottom: 30px;
  width: 100%;
  height: 50px;
}
.heading{
  font-size: 20px;
  align-items: center;
}
.footer{
  color: black;
  font-size: 20px;
}
</style>
