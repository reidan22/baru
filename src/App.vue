<template>
  <b-container fluid id="app" class="centrify">
    <AsOfTime />
  </b-container>
</template>

<script>
import AsOfTime from "@/components/AsOfTime";
export default {
  name: "App",
  components: {
    AsOfTime,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
  width: 100vw;
  margin: 0;
  padding: 0;
  /* background: rgb(198, 99, 244);*/
  background: radial-gradient(
    circle,
    rgb(79, 147, 224) 0%,
    rgb(0, 204, 255) 75%
  );
  /* background: yellow; */
  overflow: hidden;
}

.centrify {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
