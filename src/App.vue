<script setup>
import { ref } from 'vue';
const contador = ref(0)
</script>
<template>
<button @click="contador++" class="plus">Incrementar</button>
<button @click="contador--" class="less">Decrementar</button>
<button @click="contador = 0" class="reset">Resetar</button>
<p>Valor do contador é: {{ contador }}</p>
</template>
<style scoped>
button {
  color: white;
  background-color: black;
  font-weight: bold;
  border-radius: 8px;
  padding: 4%;
  margin: 3%;
  box-shadow: 3px 4px 7px black;
  cursor: pointer;
  outline: none;
}
button:active{
  background-color: white;
  
  color: black;
  transform: translateY(9px);
  box-shadow: 3px 2px 7px black;
}
.plus:hover{
background-color: skyblue;
transition: 1.2s;
color:black;
}
.less:hover{
  background-color: lightcoral;
  transition: 1.2s;
  color:black;
}
.reset:hover{
  background-color: lightyellow;
  transition: 1.2s;
  color:black;
}
</style>