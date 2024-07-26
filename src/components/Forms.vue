<script setup>
import { ref, defineEmits } from 'vue'
const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmacao = ref('')
const data = ref('')
const endereco = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const linguagens = ref('')
const bio = ref('')


const emit = defineEmits(['forms-dados', 'limpar'])

function limparDados() {
  nome.value = ""
  email.value = ""
  senha.value = ""
  confirmacao.value = ""
  data.value = ""
  endereco.value = ""
  cidade.value = ""
  estado.value = ""
  hobbies.value = ""
  linguagens.value = ""
  bio.value = ""
  
  emit('limpar', {nome: nome.value, email: email.value,  data: data.value, senha: senha.value, confirmacao: confirmacao.value, endereco: endereco.value, cidade: cidade.value, estado: estado.value, hobbies: hobbies.value, linguagens: linguagens.value, bio: bio.value,  })
}

function MostrarDados() {
  emit('forms-dados', {
    nome: nome.value,
    email: email.value,
    senha: senha.value,
    confirmacao: confirmacao.value,
    data: data.value,
    endereco: endereco.value,
    cidade: cidade.value,
    estado: estado.value,
    hobbies: hobbies.value,
    linguagens: linguagens.value,
    bio: bio.value
   
  })
}
</script>
<template>
  <div class="forms-conteiner">
    <form class="edit">

      <div class="forms">
        <label for="nome">Nome:</label>
        <input id="nome" type="text" v-model="nome" >
      </div>

      <div class="forms">
        <label for="email">Email:</label>
        <input id="email" type="email" v-model="email" >
      </div>
      <div class="forms">
        <label for="senha">Senha:</label>
        <input id="senha" type="password" v-model="senha" >
      </div>
      <div class="forms">
        <label for="confirmacao">Confirmação de Senha:</label>
        <input id="confirmacao" type="password" v-model="confirmacao">
      </div>
     
      <div class="forms">
        <label for="dataN">Data de Nascimento:</label>
        <input id="dataN" type="date" v-model="data" >
      </div>
      <div class="forms">
        <label for="endereco">Endereço:</label>
        <input id="endereco" type="text" v-model="endereco">
      </div>
      <div class="forms">
        <label for="cidade">Cidade:</label>
        <input id="cidade" type="text" v-model="cidade" >
      </div>
      <div class="forms">
        <label for="estado">Estado:</label>
        <select id="estado" v-model="estado" >
          <option value="" disabled>Selecione seu estado:</option>
          <option>AC</option>
          <option>AL</option>
          <option>AM</option>
          <option>BA</option>
          <option>CE</option>
          <option>DF</option>
          <option>ES</option>
          <option>GO</option>
          <option>MA</option>
          <option>MG</option>
          <option>MS</option>
          <option>MT</option>
          <option>PA</option>
          <option>PB</option>
          <option>PE</option>
          <option>PI</option>
          <option>PR</option>
          <option>RJ</option>
          <option>RN</option>
          <option>RO</option>
          <option>RR</option>
          <option>RS</option>
          <option>SC</option>
          <option>SE</option>
          <option>SP</option>
          <option>TO</option>
        </select>
      </div>
      <div class="forms">
        <label for="hobbies">Hobbies:</label>
        <input id="hobbies" type="text" v-model="hobbies" >
      </div>
      <div class="forms">
        <label for="linguagens">Linguagens de Programação:</label>
        <input id="linguagens" type="text" v-model="linguagens" >
      </div>
      <div class="forms">
        <label for="biografia">Biografia:</label>
        <textarea id="biografia" v-model="biografia" ></textarea>
      </div>
     
    </form>

    <div class="buttons">
      <button @click="MostrarDados">Confimarção</button>
      <button @click="limparDados" >Limpar</button>
    </div>
  </div>
</template>

<style scoped>

</style>