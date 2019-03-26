<template>
  <div id="Connect">
    <input ref="login" v-model="login" placeholder="Login">
    <button @click="connexion()">Connexion</button>
    {{login}}
  </div>
</template>

<script>
export default {
  name: 'Connect',
  data() {
     return {
        login: "",
    } 
  },
  methods: {
    connexion() {
      //debugger;
      //if (this.login == "") {
        console.log(this.$refs.login.value);
        this.login = this.$refs.login.value;
      //}
    },
  }
};
</script>

<style scoped>
#Connect {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
