<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <HomeVue/>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import HomeVue from './components/Home.vue';

export default {
  name: "App",
  components: {
    HelloWorld,
    HomeVue
  },
};
</script>
