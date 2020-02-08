<template>
  <div id="app">
    <HelloWorld :msg="message"/>
    <button @click="ChangeMessage()">1. Update Parent Model</button>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld
  },
  data() {
    return {
      message: "Default Message"
    };
  },
  methods: {
    ChangeMessage() {
      this.message = "Updated message!";
    }
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
</style>
