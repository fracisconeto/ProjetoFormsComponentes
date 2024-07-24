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

const hobbies = reactive([
  { id: 1, hobbie: 'Esporte' },
  { id: 2, hobbie: 'Ler' },
  { id: 3, hobbie: 'Cozinhar' },
  { id: 4, hobbie: 'Viajar' }
])
</script>


<template>
 <h1>Formulario</h1>

 <form >

<label for="Nome"> Digite seu nome:</label>
<input type="text">

<label for="Email">Digite o seu email:</label>
<input type="email">

<label for="Senha">Digite sua senha:</label>
<input type="password">

<label for="Confirmacao">Digite sua senha mais uma vez:</label>
<input type="password">
 
<label for="DataNacimento">Digite sua data de nascimento:</label>
<input type="date">

<label for="Idade">Digite a sua idade:</label>
<input type="number">

<label for="Estado">Selecione o seu estado:</label>

<select >
          <option v-for="estado in estados" :key="estado.sigla" :value="estado.sigla">
            {{ estado.name }}
          </option>
</select>

<label for="Cidade">Digite a sua cidade:</label>
<input type="text">

<label for="Endereco">Informe o seu endereço</label>
<input type="text">


<label for="Hobbies"> Selecione os seus hobbies</label>
<input type="checkbox" :value="passatempo.hobbie" :id="passatempo.hobbie"
          />
          <label :for="passatempo.hobbie">{{ passatempo.hobbie }}</label>
</form>

</template>


<style scoped>

</style>
