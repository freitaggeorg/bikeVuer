<template>
  <div><i class="fas fa-biking fa-flip-horizontal"></i> BikeVuer <i class="fas fa-biking "></i></div>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/accessories">Accessories</router-link>
  </div>
  <router-view/>
</template>

<style>
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
