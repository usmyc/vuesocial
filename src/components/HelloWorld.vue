<template>
  <div class="hello">
    <h1>{{ header }}</h1>
    <button @click.right="modalright" @click.left="modalleft">Click</button>
    <slot></slot>
    <slot name="links"></slot>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    header: String,
  },
  methods: {
    modalright() {
      console.log("Right");
    },
    modalleft() {
      console.log("Left");
    },
  },
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
