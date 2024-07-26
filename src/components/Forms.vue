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
  <h1>Meu Formulário de Dados</h1>
  <div class="forms-conteiner">
    <form>

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

  
.forms-conteiner {
  max-width: 600px;
  margin: 50px auto;
  padding: 40px;
  border-radius: 20px;
  background: linear-gradient(145deg, #00c6ff, #0072ff);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3);
  border: 2px solid #0072ff;
  position: relative;
  overflow: hidden;
}


.forms-conteiner::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 20% 20%, rgba(255, 255, 255, 0.15), transparent);
  opacity: 0.4;
  pointer-events: none;
  z-index: 0;
}


h1 {
  text-align: center;
  color: #0f0303;
  margin-bottom: 20px;
  font-family: 'Roboto', sans-serif;
  font-size: 2.5rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  position: relative;
  z-index: 1;
}


.forms {
  margin-bottom: 20px;
}

label {
  display: block;
  font-size: 18px;
  color: #ffffff;
  margin-bottom: 8px;
  font-family: 'Roboto', sans-serif;
  position: relative;
  z-index: 1;
}

input[type="text"],
input[type="email"],
input[type="password"],
input[type="date"],
textarea,
select {
  width: 100%;
  padding: 12px;
  border: none;
  border-radius: 8px;
  box-sizing: border-box;
  font-size: 16px;
  font-family: 'Roboto', sans-serif;
  transition: all 0.3s ease;
  background: rgba(255, 255, 255, 0.9);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  position: relative;
  z-index: 1;
}

input[type="text"]:focus,
input[type="email"]:focus,
input[type="password"]:focus,
input[type="date"]:focus,
textarea:focus,
select:focus {
  background: rgba(255, 255, 255, 1);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
  outline: none;
}


select option {
  background: #0072ff;
  color: #fff;
}


textarea {
  height: 120px;
  resize: vertical;
}

select {
  background: rgba(255, 255, 255, 0.9);
}


.buttons {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  margin-top: 30px;
}

button {
  padding: 14px 25px;
  border: none;
  border-radius: 12px;
  color: #fff;
  font-size: 18px;
  cursor: pointer;
  transition: all 0.3s ease;
  font-family: 'Roboto', sans-serif;
  width: 48%;
  position: relative;
  z-index: 1;
  overflow: hidden;
}

button::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 50%, rgba(255, 255, 255, 0.3), transparent);
  transition: all 0.3s ease;
  z-index: -1;
}

button:hover::before {
  background: radial-gradient(circle at 50%, rgba(255, 255, 255, 0.5), transparent);
}

button:first-of-type {
  background: #ff5e57;
}

button:last-of-type {
  background: #00c6ff; 
}


</style>