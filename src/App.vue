<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>
<script>
export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador() {
      if (this.contador > 0) {
      this.contador--
    }
    },  
    resetarContador() {
      this.contador = 0
    }
    
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }

}
</script>

<template>
 <button @click="incrementarContador" class="plus">Incrementar</button>
  <button @click="decrementarContador" class="less">Decrementar</button>
  <button @click="resetarContador" class="reset">Resetar</button>
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
