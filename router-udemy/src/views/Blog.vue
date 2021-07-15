<template>
  <div>
    <Titulo texto="Titulo de mi Blog" />
    <div v-for="post in arrayBlog" :key="post.id">
      <router-link :to="`/blog/${ post.id }`">{{ post.title }}</router-link>
    </div>
  </div>
</template>

<script>
import Titulo from '@/components/Titulo.vue'
export default {
  components: {
    Titulo
  },
  data () {
    return {
      arrayBlog: []
    }
  },
  mounted () {
    this.getBlogs()
  },
  methods: {
    async getBlogs () {
      try {
        const data = await fetch('https://jsonplaceholder.typicode.com/posts')
        const array = await data.json()
        this.arrayBlog = array
      } catch (err) {
        console.error(err)
      }
    }
  }
}
</script>
