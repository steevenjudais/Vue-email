<template>
<div id="Messages">
<li>
{{ msg.id }} {{ msg.title }}
</li>
</div>
</template>

<script>

export default {
  name: 'Messages',
  props:["msg"]
};
</script>

<style scoped>
#Messages {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>