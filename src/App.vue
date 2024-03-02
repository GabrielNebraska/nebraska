<script setup>

import { ref } from 'vue';

const nome = 'Gabriel'
const idade = 17
const contador = ref(0)

function inverter(texto) {
  return texto.split('').reverse().join('')
}

function saudacao() {
  return `Olá, ${nome}!`
}

function decrementar() {
  if (contador.value > 0) {
    contador.value--
  }
}

function reset() {
  contador.value = 0
}

</script>

<template>
  <div class="info">
    <h1>Exemplo 1 - Mostrando informações na tela</h1>
    <p>Nome: {{ nome }} </p>
    <p>Idade: {{ idade }} anos</p>
    <hr />
    <p>Para completar 50 anos faltam: {{ 50 - idade }} anos</p>
    <p>O nome tem {{ nome.length }} caracteres</p>
    <p>O nome invertido é: {{ inverter(nome) }} </p>
    <hr />
    <p> Exemplo de saudação usando função</p>
    <p> {{ saudacao() }} </p>
    <hr />
    <div class="contador">

      <button @click="contador++">+</button>
      <button @click=decrementar>-</button>
      <button @click="reset">C</button>
      <div v-if="contador > 10"><span style="color:green"> O contador é {{ contador }}</span></div>
      <div v-else><span style="color:red"> O contador é {{ contador }}</span></div>

    </div>
  </div>


</template>

<style scoped>
.info {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

.contador {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  align-items: baseline;

}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}

button {

  border-radius: 8px;
  padding: 2px 5px;
  border-width: 4px;
  font-size: 1.2em;


}
</style>
