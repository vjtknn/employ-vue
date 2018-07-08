<template>
  <div id="app">
    <div id="nav">
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <router-link to="/">Jobs</router-link> |
        <router-link to="/about">About</router-link> |
        <router-link to="/new">New</router-link> |
      </nav>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
@import '../node_modules/bootstrap/scss/bootstrap.scss';

.navbar a {
  color: white;
  text-decoration: none;
}
</style>
