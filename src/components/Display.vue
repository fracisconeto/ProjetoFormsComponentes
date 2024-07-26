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

.dados-container {
  max-width: 700px;
  margin: 40px auto;
  padding: 30px;
  border-radius: 15px;
  background: linear-gradient(145deg, #ffffff, #e6e6e6);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  position: relative;
  overflow: hidden;
}

.dados-container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 30% 30%, rgba(0, 0, 0, 0.05), transparent);
  opacity: 0.3;
  pointer-events: none;
  z-index: 0;
}


h2 {
  text-align: center;
  color: #333;
  margin-bottom: 20px;
  font-family: 'Roboto', sans-serif;
  font-size: 2rem;
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.2);
  position: relative;
  z-index: 1;
}


.list {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.list li {
  padding: 15px;
  border-bottom: 1px solid #ddd;
  font-family: 'Roboto', sans-serif;
  font-size: 16px;
  color: #555;
  background: rgba(255, 255, 255, 0.8);
  position: relative;
  z-index: 1;
}

.list li:last-of-type {
  border-bottom: none;
}

.list strong {
  color: #0072ff; 
}


.list li:hover {
  background: rgba(0, 114, 255, 0.1);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transform: translateY(-2px);
  transition: all 0.3s ease;
}

.list li:hover strong {
  color: #0056b3;
}

</style>