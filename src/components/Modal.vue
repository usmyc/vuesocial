<template>
  <div>
    <h1>{{ header }}</h1>
    <h3>{{ altHeader }}</h3>
    <p>{{ text }}</p>
    <button @click="changeClass">Click</button>
  </div>
</template>

<script>
export default {
  name: "Modal",
  data() {
    return {
      header: "Header",
      altHeader: "Alt-Header",
      text: "Dummy Text",
    };
  },
  methods: {
    changeClass() {
      console.log(this.header);
    },
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
h3 {
  color: blue;
}
p {
  color: green;
}
</style>
