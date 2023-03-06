<template>
  <nav>
    <router-link :to="{ name: 'home' }">Home</router-link>
    <router-link :to="{ name: 'about' }">About</router-link>
    <router-link :to="{ name: 'jobs' }">Jobs</router-link>
  </nav>
  <button @click="redirect">Redirect</button>
  <button @click="go">Go Forward</button>
  <button @click="back">Go backward</button>
  <router-view />
</template>
<script>
export default {
  methods: {
    redirect() {
      this.$router.push({ name: 'home' });
    },
    go() {
      this.$router.go(1);
    },
    back() {
      this.$router.go(-1);
    }
  }
}
</script>

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

button {
  margin: 0 10px;
  padding: 10px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>
