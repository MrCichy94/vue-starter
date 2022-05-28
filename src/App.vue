<template>
  <div id="app">
    <h1>Mail to: {{email}}</h1>
    <div class = "validate" v-if="email.length < 10">Ale masz krótki adres!</div>
    <div class = "validate" v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
    <div class = "validate" v-else>Twój adres e-mail jest stanowczo za długi.</div>
    <input type="email" v-model="email">
    <button @click="alertMyEmail()">Wyświetl mój e-mail w alercie</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: ' '
    };
  },

  methods: {
    alertMyEmail() {
      alert(this.email);
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
