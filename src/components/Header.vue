<template>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Projetos</a></li>
    <li><a href="#">Contatos</a></li>
    <li v-if="esta_logado"> <a href="https://github.com/j-ordep" target="_blank">Meu perfil</a></li>
  </ul>
</template>

<script>
export default {
  name: "Header",
  props: ["esta_logado"]
}
</script>

<style scoped>
ul {
  list-style: none;
  display: flex;
  background: #444444;
}

li{
  margin-right: 10px;
}

a {
  color: #ddd;
  text-decoration: none;
  transition: .5s;
}

a:hover {
  color: rgb(255, 193, 23);
}
</style>