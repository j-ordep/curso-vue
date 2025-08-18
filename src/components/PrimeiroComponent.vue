<template>
  <div>
    <h1>Olá Mundo</h1>
    <p>Meu nome é {{ nome }}, sou um {{ profissao }}</p>
    <Reutilizacao/>
    <MultiEventos/>
    <Reutilizacao/>
  </div>
</template>

<script>
import MultiEventos from './MultiEventos.vue';
import Reutilizacao from './Reutilizacao.vue';

export default {
  name: "PrimeiroComponent",
  components: {
    MultiEventos,
    Reutilizacao,
  },
  data() {
    return {
      nome: "J",
      profissao: "Dev"
    }
  }
}
</script>
