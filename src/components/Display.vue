<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  nome: String,
  email: String,
  confirmacao: String,
  mostrar: Boolean,
  dataN: String,
  endereco: String,
  cidade: String,
  estado: String,
  hobbies: String,
  linguagens: String,
  biografia: String,
  senha: String,
 
})
</script>
<template>
  <div v-if="mostrar" class="dados-container">
    <h2>Dados do Usuário</h2>
    <ul class="list">

      <li><strong>Nome:</strong> {{ nome }}</li>
      <li><strong>Email:</strong> {{ email }}</li>
      <li><strong>Senha:</strong> {{ senha }}</li>
      <li><strong>Confirmação de Senha:</strong> {{ confirmacao }}</li>
      <li><strong>Data de Nascimento:</strong> {{ dataN }}</li>
      <li><strong>Endereço:</strong> {{ endereco }}</li>
      <li><strong>Cidade:</strong> {{ cidade }}</li>
      <li><strong>Estado:</strong> {{ estado }}</li>
      <li><strong>Hobbies:</strong> {{ hobbies }}</li>
      <li><strong>Linguagens de Programação:</strong> {{ linguagens }}</li>
      <li><strong>Biografia:</strong> {{ biografia }}</li>
    
    </ul>
  </div>
</template>



<style scoped>

</style>