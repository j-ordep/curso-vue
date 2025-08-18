<template>
  <img :src="avatar" :alt="descricao"> <!-- " : " é igual a v-bind -->

  <MudarImg @mudar-imagem="trocarImagem"/>
</template>

<script>
import MudarImg from './MudarImg.vue';

export default {
  name: "Picture",
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "foto do avatar"
    } 
  },
  components: {
    MudarImg,
  },
  methods: {
    trocarImagem() {
      this.avatar = "/img/avatar2.png"
    }
  }
}
</script>