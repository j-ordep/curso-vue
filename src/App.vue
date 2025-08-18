<template>
  <div>
    <Header/>
    <LifeCycle />
    <p class="teste-pai">teste component pai</p>
    <Pessoa/>
  </div>
</template>

<script>
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue';
import Header from './components/Header.vue';

export default {
  name: 'App',
  components: {
    Header,
    LifeCycle,
    Pessoa,
  }
}
</script>

<style>
body {
  background-color: #333;
  color: #fff
}

a {
  color: red;
}

.teste {
  background-color: #000;
}
</style>