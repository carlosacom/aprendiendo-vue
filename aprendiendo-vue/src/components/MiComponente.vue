<template>
  <div id="mi-componente">
    <h1>Este es mi componente</h1>
    <h2>{{ subtitle }}</h2>
  </div>
</template>
<script>
export default {
  name: "MiComponente",
  data: () => {
    return {
      subtitle: "Soy un subtitulo",
    };
  },
};
</script>