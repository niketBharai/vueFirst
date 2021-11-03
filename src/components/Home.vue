<template>
  <h1>Hello {{ username }}</h1>
  <input type="text" placeholder="Enter Email"/>
  <br />
  <br />
  <input type="text" v-model="count" placeholder="Enter username"/>
  <br />
  <br />
  <button v-on:click="handleClick()">Get Values</button>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      username: "Niket Bharai",
      count: 0,
    };
  },
  methods: {
    handleClick() {
      this.count = this.count + 1;
    },
  },
};
</script> 