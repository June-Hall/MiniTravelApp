<template>
  <div class="home">
    <div v-for="destination in destinaitons" :key="destination.name">
      <router-link to="destination.slug"></router-link>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import store from "@/store.js";
export default {
  name: "HomeView",
  components: {},
  data() {
    return {
      destinaitons: store.destinations,
    };
  },
};
</script>
