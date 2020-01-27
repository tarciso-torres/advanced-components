<template>
  <div id="app" class="container">
    <h1>Componentes dinâmicos</h1>

    <button @click="componenteSelecionado = 'Home'">Home</button>
    <button @click="componenteSelecionado = 'PostsLista'">PostsLista</button>
    <button @click="componenteSelecionado = 'Sobre'">Sobre</button>

    <p>{{ componenteSelecionado }}</p>

    <component :is="componenteSelecionado"></component>
    
    
  </div>
</template>

<script>
import Home from './components/Home.vue'
import PostsLista from './components/PostsLista.vue'
import Sobre from './components/Sobre.vue'

export default {
  name: 'app',
  components: {
    Home,
    PostsLista,
    Sobre
  },
  data() {
    return {
      componenteSelecionado: 'Home',
      posts: [
        { id: 1, titulo: 'Components no Vue', conteudo: 'Componentes são uma das peças mais importantes no vue', autor: 'Tarciso Torres'},
        { id: 2, titulo: 'Distribuindo conteúdo com Slots', conteudo: 'Slots podem ser usados como repositórios de código HTML', autor: 'Tarciso Torres'}
      ]
    }
  }
}
</script>

<style scoped>
  .container {
    width: 960px;
    margin: auto;
  }

</style>


