<template>
  <div>
    <Header />
    <PrimeiroComponente />
    <p>O dado de App é: {{ teste }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
  import Header from './components/Header.vue'
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'

  export default {
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Header
    },
    data() {
      return {
        teste: "testando dados pelo componente root"
      }
    }
  }
</script>

<style>
  body {
    background-color: #333;
    color: #FFF;
  }
</style>