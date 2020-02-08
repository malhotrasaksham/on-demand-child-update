<template>
  <div class="hello">
    <h1>{{ computedMessage }}</h1>
    <button @click="UpdateModel()">2. Update Child Model</button>
    <br>
    <br>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      computedMessage: ""
    };
  },
  watch: {
    msg(to, from) {
      console.log("Message changed!");
    }
  },
  methods: {
    UpdateModel() {
      this.computedMessage = this.msg;
    }
  },
  created() {
    this.computedMessage = this.msg;
  },
  beforeUpdate() {
    console.log("Before update fired");
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
