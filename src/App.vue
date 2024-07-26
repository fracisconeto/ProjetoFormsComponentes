<script setup>
import { ref } from 'vue'
import Forms from './components/Forms.vue'
import Display from './components/Display.vue'

const dados = ref({
  email: '',
  nome: '',
  dataN: '',
  endereco: '',
  cidade: '',
  estado: '',
  hobbies: '',
  linguagens: '',
  biografia: '',
  senha: '',
  confirmacao: ''
})

const mostrarDados = ref(false)

function handleMostrarDados(dadosFormulario) {
  dados.value = dadosFormulario
  mostrarDados.value = true
}

function handleDadosLimpos() {
  dados.value = {
    email: '',
    nome: '',
    dataN: '',
    endereco: '',
    cidade: '',
    estado: '',
    hobbies: '',
    linguagens: '',
    biografia: '',
    senha: '',
    confirmacao: ''
  }
  mostrarDados.value = false
}
</script>
<template>
  <div id="app">
    <h1 class="text-center">Meu Formulário de Dados</h1>
    <Forms
      @mostrarDados="handleMostrarDados"
      @dadosLimpos="handleDadosLimpos"
    />
    <Display
      :email="dados.email"
      :nome="dados.nome"
      :dataN="dados.dataN"
      :endereco="dados.endereco"
      :cidade="dados.cidade"
      :estado="dados.estado"
      :hobbies="dados.hobbies"
      :linguagens="dados.linguagens"
      :biografia="dados.biografia"
      :senha="dados.senha"
      :confirmacao="dados.confirmacao"
      :mostrar="mostrarDados"
    />
  </div>
</template>


<style>

</style>