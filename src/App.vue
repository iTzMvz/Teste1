<script setup>
import { ref } from 'vue';
const contador = ref(0)
</script>
<template>
<button @click="contador++" id="plus">Incrementar</button>
<button @click="contador--" id="less">Decrementar</button>
<button @click="contador = 0" id="reset">Resetar</button>
<p>Valor do contador é: {{ contador }}</p>
</template>
<style>
body{
  background-color: rgb(17, 16, 16);
}
button {
  color: white;
  background-color: rgb(3, 3, 2);
  font-weight: bold;
  border-radius: 8px;
  padding: 6%;
  margin: 4%;
  box-shadow: 0px 0px 8px whitesmoke;
}
button:active{
  background-color: white;
  color: black;
  transform: translateY(4px);
  box-shadow: 0px 0px 9px whitesmoke;
}
#plus:hover{
background-color: skyblue;
transition: 1.2s;
color:black;
}
#less:hover{
  background-color: lightcoral;
  transition: 1.2s;
  color:black;
}
#reset:hover{
  background-color: lightyellow;
  transition: 1.2s;
  color:black;
}

</style>