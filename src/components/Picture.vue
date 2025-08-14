<template>
  <img :src="avatar" :alt="descricao"> <!-- " : " é igual a v-bind -->
</template>

<script>
export default {
  name: "Picture",
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "foto do avatar"
    } 
  }
}
</script>