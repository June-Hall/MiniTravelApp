<template>
  <nav id="nav">
    <p class="logo">The Travel App</p>
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
      destination: store.destinations,
    };
  },
};
</script>

<style scoped>
#nav {
  display: flex;
}

#nav {
  padding: 30px;
}

#nav a {
  color: #2c3e50;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #ab26ab;
}
</style>
