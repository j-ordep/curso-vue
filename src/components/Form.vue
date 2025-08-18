<template>
  <div>
    <h2>meu formulario</h2>
    <form action="" @submit="enviarFormulario($event)">
      <div>
        <input type="text" v-model="name">
      </div>
      <div>
          <input type="text" v-model="email">
      </div>
      <div>
        <InputSubmit />
      </div>
    </form>
  </div>
</template>

<script>
import InputSubmit from './form/InputSubmit.vue';
import InputText from './form/InputText.vue';

export default {
  name: "Form",
  components: {
    InputText,
    InputSubmit
  },
  data() {
    return {
      name: "",
      email: ""
    }
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault()

      const name = this.name
      const email = this.email

      console.log("formulario enviado")
      console.log("o nome é: " + name)
      console.log("o email é: " + email)

    },
  }
}
</script>