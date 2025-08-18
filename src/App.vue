<template>
  <div>
    <PrimeiroComponent/>
    <Header :esta_logado="esta_logado"/>
    <LifeCycle />
    <p class="teste-pai">teste component pai</p>
    <Pessoa/>
  </div>
</template>

<script>
import PrimeiroComponent from './components/PrimeiroComponent.vue';
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue';
import Header from './components/Header.vue';

export default {
  name: 'App',
  data() {
    return {
      esta_logado: true,
    }
  },
  components: {
    Header,
    LifeCycle,
    Pessoa,
    PrimeiroComponent,
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