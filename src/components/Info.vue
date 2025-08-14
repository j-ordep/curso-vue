<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de uma oportunidade de emprego</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
      <li>Go</li>
      <li>Java</li>
      <li>JavaScript</li>
    </ul>
    <p v-show="mostrar_email">E-mail: {{ email }}</p>
  </div>
  <div >
    
  </div>
</template>

<script>

export default {
  name: "Info",
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: true,
      email: "email@gmail.com"
    }
  }
}
</script>