<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
body {
  background: #0e0b1c;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
* {
  margin: 0;
  padding: 0;
  list-style: none;
}
.clearfix {
  zoom: 1;
}
.clearfix::after,
.clearfix::before {
  content: "";
  display: block;
  clear: both;
  visibility: hidden;
  height: 0;
}
</style>
