<script setup>
import { ref } from 'vue'
import Forms from './components/Forms.vue'
import Display from './components/Display.vue'

const dados = ref({
  nome: '',
  email: '',
  senha: '',
  confirmacao: '',
  data: '',
  endereco: '',
  cidade: '',
  estado: '',
  hobbies: '',
  linguagens: '',
  bio: '',
 
})

const mostrar = ref(false)

function handleforms(dadosFormulario) {
  dados.value = dadosFormulario
  mostrar.value = true
}

function handlemostrar() {
  dados.value = {
    nome: '',
    email: '',
    senha: '',
    confirmacao: '',
    data: '',
    endereco: '',
    cidade: '',
    estado: '',
    hobbies: '',
    linguagens: '',
    bio: '',
    
  }
  mostrar.value = false
}
</script>
<template>
  <div id="app">
    <h1 class="text-center">Meu Formulário de Dados</h1>
    <Forms
      @mostrar="handleforms"
      @dadosLimpos="handlemostrar"
    />
    <Display
      :nome="dados.nome"
      :email="dados.email"
      :senha="dados.senha"
      :confirmacao="dados.confirmacao"
      :data="dados.data"
      :endereco="dados.endereco"
      :cidade="dados.cidade"
      :estado="dados.estado"
      :hobbies="dados.hobbies"
      :linguagens="dados.linguagens"
      :bio="dados.bio"
     
      :mostrar="mostrar"
    />
  </div>
</template>


<style>

</style>