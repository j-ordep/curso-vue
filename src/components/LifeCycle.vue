<template>
  <h1>Meu nome é {{ nome }}</h1>
</template>

<script>
export default {
  name: 'LifeCycle',

  data() {
    return { 
      nome: "Ainda não sei"
    }
  },

  created() {
    setTimeout(() => {
      this.nome = "carregando"
    }, 1000);

    this.lifeCycleExec()
  },

  mounted() {
    setTimeout(() => {
      this.nome = "Juliana"
    }, 2000);

    this.lifeCycleExec()
  },

  methods: {
    lifeCycleExec() {
      console.log("executou")
    }
  }
}
</script>