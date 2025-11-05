<template>
  <div id="app" class="container">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/quotes">Random Quotes</router-link> |
      <router-link to="/contact">Contact</router-link>
    </nav>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container {
  text-align: center;
  font-family: Arial, sans-serif;
  margin-top: 50px;
}
nav a {
  margin: 0 6px;
}
</style>
