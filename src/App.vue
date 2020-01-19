<template>
  <div id="app">
    <h1>Vue js</h1>
    <Post>
      <h2>Components no Vue</h2>
      <p>Componentes são uma das peças mais importantes no Vue</p>
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


