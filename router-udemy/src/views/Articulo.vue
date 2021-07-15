<template>
  <div v-if="post">
    <Titulo :texto="post.title"/>
    <p>{{ post.body }}</p>
  </div>
  <div v-else>No existe el post</div>
</template>

<script>
import Titulo from '../components/Titulo.vue'
export default {
  name: 'Articulo',
  components: {
    Titulo
  },
  data () {
    return {
      post: null
    }
  },
  mounted () {
    this.getPost(this.$route.params.id)
  },
  methods: {
    async getPost (id) {
      try {
        const data = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`)
        const post = await data.json()
        this.post = post
      } catch (err) {
        console.error(err)
      }
    }
  }
}
</script>
