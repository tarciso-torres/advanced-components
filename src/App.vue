<template>
  <div id="app" class="container">
    <h1>Forma Padrão</h1>
    <PostsLista :posts="posts" />

    <hr>

    <h1>Slots com escopo</h1>

    <PostsLista :posts="posts">
      <template slot-scope="slotProps">
        <h2>{{ slotProps.meuPost.titulo }}</h2>
        <p>{{ slotProps.meuPost.conteudo }}</p>
        <small>{{ slotProps.meuPost.autor }}</small>
      </template>
    </PostsLista>
    
  </div>
</template>

<script>
import PostsLista from './components/PostsLista.vue'

export default {
  name: 'app',
  components: {
    PostsLista
  },
  data() {
    return {
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


