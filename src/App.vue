<template>
  <div id="app" class="container">
    <h1>Vue js</h1>
    <Post>
      <h2 slot="cabecalho">Components no Vue</h2>
      <template slot="conteudo">
        <p>Componentes são uma das peças mais importantes no Vue</p>
        <span>...</span>
      </template>
      <small slot="rodape">Por Tarciso Torres</small>
    </Post>
  </div>
</template>

<script>
import Post from './components/Post.vue'

export default {
  name: 'app',
  components: {
    Post
  }
}
</script>

<style scoped>
  .container {
    width: 960px;
    margin: auto;
  }
</style>


