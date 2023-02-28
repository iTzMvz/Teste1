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
 <button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <button @click="resetarContador">Resetar</button>
  <p>Valor do contador é: {{ contador }}</p>
</template>

<style scoped>
button {
  font-weight: bold;
  border-radius: 8px;
}
</style>
