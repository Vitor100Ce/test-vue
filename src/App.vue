<template>

<div>


  <Header/>
  <!-- <PrimeiroComponente /> -->
  <p class="paragrafo-pai">O teste {{ testando }}</p>
  <LifeCycle/>
  <Pessoa/>


</div>
  
</template>

<script>

import LifeCycle from './components/LifeCycle.vue'
// import PrimeiroComponente from './components/PrimeiroComponente.vue'
import Pessoa from './components/Pessoa.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components:{
    // PrimeiroComponente,
    LifeCycle,
    Pessoa,
    Header
  },
  data(){
    return{
      testando: 'Teste'
    }
  }
}
</script>

<style>

  body{
    background: #333;
    color: #fff;
  }

  a{
    color: red;
  }

  .teste{
    background-color: black;

  }

  .paragrafo-pai{
    color: red;
  }

</style>
