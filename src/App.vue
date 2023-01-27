<template>
  <div class="logo-image">
    <img alt="Vue logo" src="./assets/logo.png" width="200" />
  </div>
  <HelloWorld :header="appname">
    <h1>Blog Fighter</h1>
    <p>Grab your fighter swag for half price!</p>
    <template v-slot:links> 
      <a href="#" class="button">Click me!</a>
    </template>
  </HelloWorld>

  <Modal/>

  <div class="sendbutton">
    <p>header:</p>
    <input type="text" ref="header" />
    <p>text:</p>
    <input type="text" ref="data" />
    <button class="button" @click="send">Send</button>
  </div>

  <div class="formdata">
    <h1>{{ formhead }}</h1>
    <p>{{ formtext }}</p>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  data() {
    return {
      appname: "MetaSocial",
      formhead: "",
      formtext: "",
    };
  },

  methods: {
    send() {
      this.formhead = this.$refs.header.value;
      this.formtext = this.$refs.data.value;
    },
  },

  components: {
    HelloWorld,
    Modal,
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
  gap: 1.5rem;
}
.logo-image {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 200px;
  border-radius: 100%;
  overflow: hidden;
}
.sendbutton {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}
.button {
  color: #ffffff;
  background-color: indigo;
  padding: 10px 1rem;
  border-radius: 10px;
  text-decoration: none;
  box-shadow: 0 10px 1rem 0 rgba(0, 0, 0, 0.2);
  cursor: pointer;
}
.button:hover {
  background-color: rgb(194, 150, 226);
}
.formdata {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

</style>
