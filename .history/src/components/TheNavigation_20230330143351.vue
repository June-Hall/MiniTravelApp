<template>
  <nav id="nav">
    <p></p>
    <ul class="nav-links">
      <li class="links">
        <router-link to="/"> Home </router-link>
      </li>
      <li
        v-for="destination in destinations"
        :key="destination.name"
        class="links"
      >
        <router-link
          to="{name: 'DestinationDetails', params:
        {id:destination.id}}"
        >
          {{ destination.name }}</router-link
        >
      </li>
    </ul>
  </nav>
</template>

<script>
import store from "@/store.js";
export default {
  data() {
    return {
      destinationId: this.$route.params.id,
      destination: store.destinatons,
    };
  },
};
</script>

<style scoped>
#nav {
  display: flex;
  justify-content: center;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 0 10px;
}

nav a.router-link-exact-active {
  color: #ab26ab;
}
</style>
