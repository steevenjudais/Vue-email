<template>
<div id="TopBar">
<Connect/>
<SendMessage/>
</div>
</template>

<script>
import Connect from './Connect.vue';
import SendMessage from './SendMessage.vue';

export default {
  name: 'TopBar',
  components: {
    Connect,
    SendMessage,
  },
};
</script>

<style scoped>
#TopBar {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
