<script setup>

import {ref} from 'vue'

const contador = ref(0)

function decrementar(){
  contador.value--
}

</script>

<template>



<button @click="contador++">adicionar</button>
<button @click="contador--">decrementar</button>
 <p>O valor do contador é {{ contador }}</p>
</template>

<style scoped>
</style>
