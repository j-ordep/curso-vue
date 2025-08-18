<template>
  <div>
    <button @click="primeiro(txt1, $event), segundo($event), terceiro($event)">Ativar Multiplos Eventos</button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script>
export default {
  name: "MultiEventos",
  data() {
    return {
      multiplos_eventos: "",
      txt1: "primeiro evento ativado"
    }
  },
  methods: {
    primeiro(txt, e) {
      this.multiplos_eventos = txt // texto vem do data() e é passado como parametro no evento do html
    },
    segundo(e) {
      setTimeout(() => {
        this.multiplos_eventos = "segundo evento ativado"
      }, 800)
    },
    terceiro(e) {
      setTimeout(() => {
        this.multiplos_eventos = ""
      }, 1500)
    },
  }
}
</script>

<style scoped>
div {
  margin: 100px;
}
</style>