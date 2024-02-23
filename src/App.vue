<script setup>

import {ref} from 'vue'

const contador = ref(0)


function decrementar(){  
  if (contador.value > 0){  
  contador.value--
}

}

function reset(){
  contador.value = 0
}
</script>

<template>
   


<button @click="contador++">adicionar</button>
<button @click="decrementar">decrementar</button>
<button @click="reset">Resetar</button>

<p>O valor do contador é {{ contador }}</p>

</template>

<style scoped>
button {
font-size: 2rem;
padding: 1rem;
margin: 1rem;
cursor: pointer;
border: none;
background-color: aliceblue;
border-radius: 0.5rem;


}
</style>
