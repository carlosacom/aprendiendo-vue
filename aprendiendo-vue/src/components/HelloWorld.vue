<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ helloWorld }}</h2>
    <p>{{ paraph }}</p>
    <div style="background-color:red">
      <MiComponente />
    </div>
  </div>
</template>

<script>
import MiComponente from "./MiComponente.vue";

export default {
  name: "HelloWorld",
  components: {
    MiComponente,
  },
  props: {
    msg: String,
  },
  data: () => {
    return {
      helloWorld: "Hola mundo pues",
      paraph:
        "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of L",
    };
  },
};
</script>
