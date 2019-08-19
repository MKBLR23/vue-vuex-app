<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <appCounter />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import appCounter from "@/components/counter.vue";

export default {
  name: "home",
  components: {
    HelloWorld,
    appCounter
  }
};
</script>
