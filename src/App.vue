<template>
  <div class="logo-image">
    <img alt="Vue logo" src="./assets/logo.png" width="200" />
  </div>

  <HelloWorld :header="appname" />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      appname: "MetaTurkiye Social",
    };
  },
  components: {
    HelloWorld,
  },
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  align-items: center;
  color: #2c3e50;
  margin-top: 60px;
}
.logo-image {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 200px;
  border-radius: 100%;
  overflow: hidden;
}
</style>
