<template>
  <div id="app">
    <div v-if="!isAuthenticated">
      <h1>WITAJ W EKRANIE LOGOWANIA</h1>
      <h1>Mail to: {{email}}</h1>
      <div class = "validate" v-if="email.length < 10">Ale masz krótki adres!</div>
      <div class = "validate" v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
      <div class = "validate" v-else>Twój adres e-mail jest stanowczo za długi.</div>
      <input type="email" v-model="email" @keyup.enter = "logIn()">
      <button @click="logIn()">Zaloguj</button>
    </div>
    <div v-else>
      <h1>Witaj na zajęciach {{email}}!</h1>
      <button @click="logOut()">Wyloguj</button>
    </div>
  </div>
</template>

<script>
import "milligram";
export default {
  data() {
    return {
      email: ' ',
      isAuthenticated: false
    };
  },

  methods: {
    logIn() {
      this.isAuthenticated = true;
    },
    logOut() {
      this.isAuthenticated = false;
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
  margin-top: 60px;
}

.validate {
  color: red;
}
</style>
