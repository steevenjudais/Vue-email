<template>
<div class="colonne1" id="LeftBar">
<Messages v-for="messages in message" :msg="messages"/>
</div>
</template>

<script>
import Messages from './Messages.vue';
import axios from 'axios';

export default {
  name: 'LeftBar',
  components: {
    Messages,
  },
  data() {
     return {
         message: [
            //{ id: 1, expediteur: "moi", destinataire: "toi", message: "message", date: "ajd"}
            //{ item: 'Foo' },
            //{ item: 'Bar' },
            //{ item: 'abc' },
            //{ item: 'def' },
            //{ item: 'ghi' },
            //{ item: 'jkl' }
        ]
     }
  },
  async mounted() {
      const reponse = await axios.get('https://jsonplaceholder.typicode.com/todos');
      this.message = reponse.data;
  }
};
</script>

<style scoped>
#LeftBar {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.colonne1 {
  width:25%;
  float:left;
  position: relative; 
}
</style>
