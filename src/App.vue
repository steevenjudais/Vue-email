<template>
  <div :style="{backgroundColor: bgColor}" id="app">
    <!-- <button @click="start()">Stroboscope</button> -->
    <TopBar></TopBar>
    <LeftBar/>
    <RightBar/>
  </div>
</template>

<script>
import TopBar from './components/TopBar.vue';
import LeftBar from './components/LeftBar.vue';
import RightBar from './components/RightBar.vue';

export default {
  name: 'app',
  components: {
    TopBar,
    LeftBar,
    RightBar,
  },
  data() {
     return {
        login: "",
        etat: false,
        listeColors:["red", "yellow", "green", "blue"],
        bgColor:"white",
        x: null,
        i:3,
      } 
  },
  methods: {
    strombo() {
      if (this.i == -1) {
        this.i = 3;
      }
      this.bgColor = this.listeColors[this.i];
      this.i--;
    },
    start() {
      if (this.etat == true) {
        this.etat = false;
        clearInterval(this.x);
      } else if (this.etat == false) {
        this.etat = true;
        this.x = setInterval(this.strombo, 50);
      }
    },
    connexion() {
      //if (this.login == "") {
        //console.log(this.$refs.login.value);
        //this.login = this.$refs.login.value;
      //}
    },
  }
};

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.colonne1 {
  width:25%;
  float:left;
  position: relative; 
}
.colonne2 {
  width:74%;
  float:left;
  position: relative; 
}
</style>
