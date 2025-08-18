<template>
  <div>
    <h2>Descrição da pessoa {{ nome }}</h2>
    <Info :email="email" :esta_trabalhando="esta_trabalhando"/>
    <Form/>
  </div>
</template>

<script>
import Info from './Info.vue';
import Form from './Form.vue';

export default {
  name: "Pessoa",
  components: {
    Info,
    Form
  },
  data() {
    return {
      nome: "Juliana",
      email: "ju@email.com",
      esta_trabalhando: true,
    }
  }
}
</script>