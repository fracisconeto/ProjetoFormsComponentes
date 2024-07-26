<script setup>
// const emit = defineEmits(['salvar'])
const estados = [
  { sigla: 'AC', name: 'Acre' },
  { sigla: 'AL', name: 'Alagoas' },
  { sigla: 'AP', name: 'Amapá' },
  { sigla: 'AM', name: 'Amazonas' },
  { sigla: 'BA', name: 'Bahia' },
  { sigla: 'CE', name: 'Ceará' },
  { sigla: 'DF', name: 'Distrito Federal' },
  { sigla: 'ES', name: 'Espírito Santo' },
  { sigla: 'GO', name: 'Goiás' },
  { sigla: 'MA', name: 'Maranhão' },
  { sigla: 'MT', name: 'Mato Grosso' },
  { sigla: 'MS', name: 'Mato Grosso do Sul' },
  { sigla: 'MG', name: 'Minas Gerais' },
  { sigla: 'PA', name: 'Pará' },
  { sigla: 'PB', name: 'Paraíba' },
  { sigla: 'PR', name: 'Paraná' },
  { sigla: 'PE', name: 'Pernambuco' },
  { sigla: 'PI', name: 'Piauí' },
  { sigla: 'RJ', name: 'Rio de Janeiro' },
  { sigla: 'RN', name: 'Rio Grande do Norte' },
  { sigla: 'RS', name: 'Rio Grande do Sul' },
  { sigla: 'RO', name: 'Rondônia' },
  { sigla: 'RR', name: 'Roraima' },
  { sigla: 'SC', name: 'Santa Catarina' },
  { sigla: 'SP', name: 'São Paulo' },
  { sigla: 'SE', name: 'Sergipe' },
  { sigla: 'TO', name: 'Tocantins' }
]
// function handleSubmit(){
//   emit('salvar', ???)
// }

</script>


<template>
  
  <h1>Formulario</h1>

  <form>
    <div class="container-forms">

    <label for="Nome"> Digite seu nome:</label>
    <input type="text">

    <label for="Email">Digite o seu email:</label>
    <input type="email">

    <label for="Senha">Digite sua senha:</label>
    <input type="password">

    <label for="Confirmacao">Digite sua senha mais uma vez:</label>
    <input type="password">

    <label for="DataNacimento">Digite sua data de nascimento:</label>
    <input type="date"></div>

    <label for="Estado">Selecione o seu estado:</label>

    <select>
      <option v-for="estado in estados" :key="estado.sigla" :value="estado.sigla">
        {{ estado.name }}
      </option>
    </select>

    <label for="Cidade">Digite a sua cidade:</label>
    <input type="text">

    <label for="Endereco">Informe o seu endereço</label>
    <input type="text">

   <div class="container-hobbies"> 
<label for="hobbies">Selecione os seus hobbie:</label>
      <div>
        <input type="checkbox" id="esporte">
        <label for="Sport">Esporte</label>

      </div>
      <div>
        <input type="checkbox" id="ler">
        <label for="read">Ler </label>
      </div>
      <div>
        <input type="checkbox" id="cozinhar">
        <label for="cook">Cozinhar</label>
      </div>
      <div>
        <input type="checkbox" id="viajar">
        <label for="travel">Viajar</label>
      </div>
    

    <label for="linguagens">Selecione os seus:</label>
      <div>
        <input type="checkbox" id="Java">
        <label for="java">Java</label>

      </div>
      <div>
        <input type="checkbox" id=" C++">
        <label for="c++">C++</label>
      </div>
      <div>
        <input type="checkbox" id="Python">
        <label for="python">Python</label>
      </div>
      <div>
        <input type="checkbox" id="PHP">
        <label for="php">PHP</label>
      </div>
    </div>

<button @click="handleSubmit">enviar</button>


  </form>
</template>


<style scoped>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
  color: #333;
  padding: 20px;
}


h1 {
  text-align: center;
  color: #333;
  margin-bottom: 20px;
}


form {
  max-width: 600px;
  margin: auto;
  background: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}


label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
  color: #333;
}


input[type="text"],
input[type="email"],
input[type="password"],
input[type="date"],
select {
  width: 100%;
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 16px;
}


.container-hobbies div,
.container-hobbies div input[type="checkbox"],
.container-hobbies div label {
  display: inline-block;
  margin-right: 15px;
  vertical-align: middle;
}

input[type="checkbox"] {
  margin-right: 5px;
}


button {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #5cb85c;
  color: #fff;
  border: none;
  border-radius: 4px;
  font-size: 18px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #4cae4c;
}


.container-hobbies {
  margin-bottom: 20px;
}

</style>
