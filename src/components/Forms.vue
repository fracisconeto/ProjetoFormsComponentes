<script setup>
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




  </form>
</template>


<style scoped>
.container-form{
  height: 500px;
  width: 500px;
  text-align: center;
}
</style>
