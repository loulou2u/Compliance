<template>
  <div id="app">
    <i class="material-icons icon-image-list">view_list</i> <Compliance />
  </div>
</template>

<script>
import Compliance from "./components/Compliance";

export default {
  name: "App",
  components: {
    Compliance
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.icon-image-list {
  font-size: 64px;
}
</style>

