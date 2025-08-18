<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de uma oportunidade de emprego</p>

    <p>Utilizo as seguintes tecnologias para backend:</p>
    <ul>
      <li v-for="(technology, index) in backend_technologies" v-bind:key="index">{{ technology }}</li>
    </ul>
    <p>Utilizo as seguintes tecnologias para frontend:</p>
    <ul>
      <li v-for="technology in frontend_technologies">
        {{ technology.id}} - {{ technology.language }}
      </li>
    </ul>

    <div>
      <button @click="showEmail">{{ bnt_text }}</button>
    </div>

    <p v-show="mostrar_email">E-mail: {{ email }}</p>
    <p class="teste">para acessar meu portifolio <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>
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

  props: {
    email: String,
    esta_trabalhando: Boolean
  },

  data() {
    return {
      mostrar_email: false,

      meu_link: "http://google.com",
      bnt_text: "mostrar email",

      backend_technologies: ["Go", "Java", "JavaScript"],
      frontend_technologies: [
        {id: 1, language: "HTML"},
        {id: 2, language: "CSS"},
        {id: 3, language: "Vue"},
      ]
    }
  },

  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
      if (this.mostrar_email == false) {
          this.bnt_text = "mostrar email"
      } else {
          this.bnt_text = "esconder email"
        }
    }
  }, 
  
}
</script>

<!-- não recomendado pois gera bagunça -->
<style> 
.teste-pai {
  color: aqua;
}
</style>