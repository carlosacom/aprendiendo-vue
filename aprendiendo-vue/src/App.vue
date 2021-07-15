<template>
<div>
  <Header/>
  <Slider/>
  <div class="row">
    <div class="col-md-8"></div>
    <div class="col-md-4">
      <Sidebar/>
    </div>
  </div>
</div>
</template>

<script>
import Header from "./components/Header.vue";
import Slider from "./components/Slider.vue";
import Sidebar from "./components/Sidebar.vue";

export default {
  name: "App",
  components: {
    Header,
    Slider,
    Sidebar
  },
};
</script>