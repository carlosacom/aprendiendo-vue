<template>
  <div class="home">
    <Titulo texto="Página de inicio"/>
    <img alt="Vue logo" src="../assets/logo.png">
  </div>
</template>

<script>
// @ is an alias to /src
import Titulo from '@/components/Titulo.vue'

export default {
  name: 'Home',
  components: {
    Titulo
  }
}
</script>
