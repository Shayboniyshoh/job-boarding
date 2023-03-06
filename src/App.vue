<template>
  <nav>
    <router-link :to="{ name: 'home' }">Home</router-link>
    <router-link :to="{ name: 'about' }">About</router-link>
    <router-link :to="{ name: 'jobs' }">Jobs</router-link>
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #fff;
  text-decoration: none;
  padding: 12px 20px;
  margin: 0.5rem 1rem;
  background: #555;
  border-radius: 8px;
  font-weight: 400;
  text-transform: uppercase;
}

nav a.router-link-exact-active {
  color: #fff;
  background: #42b983;
}
</style>
