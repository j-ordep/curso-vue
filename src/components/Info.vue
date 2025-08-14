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
    <div>
      <button @click="showEmail">Mostrar email</button>
    </div>
    <p v-show="mostrar_email">E-mail: {{ email }}</p>
    <p>para acessar meu portifolio <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>
  </div>

  <Picture/>
</template>

<script>
import Picture from './Picture.vue';

export default {
  name: "Info",
  components: {
    Picture,
  },
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: true,
      email: "email@gmail.com",
      meu_link: "http://google.com",
    }
  },
  methods: {
    showEmail() {
        this.mostrar_email = !this.mostrar_email
    }
  }, 
  
}
</script>