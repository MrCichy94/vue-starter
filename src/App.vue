<template>
  <div id="app">
    <h1>Mail to: {{email}}</h1>
    <input type="email" v-model="email">
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: ' '
    };
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
  margin-top: 60px;
}
</style>
