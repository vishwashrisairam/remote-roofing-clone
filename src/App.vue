<template>
  
  <div id="app">
    <TheNavigation/>
    <router-view/>
  </div>
</template>
<script>
import TheNavigation from '@/components/TheNavigation';
export default {
  components:{
    TheNavigation
  }
}
</script>
<style>
@import "https://stackpath.bootstrapcdn.com/bootstrap/4.1.2/css/bootstrap.min.css";
@import "https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css";

body {
	font-family: Arial,sans-serif;
	font-size: 14px;
	line-height: 20px;
	color: #333;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
