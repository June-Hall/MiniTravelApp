<template>
  <div class="home">
    <h1>All Desinations</h1>
    <div class="destinations">
      <div v-for="destination in destinations" :key="destination.name">
        <router-link :to="destination.slug">
          <h2>{{ destinaitons.name }}</h2>
        </router-link>
        <figure>
          <router-link :to="destination.name">
            <img
              :src="require(`@/assets/${destination.image}`)"
              :alt="destination.name"
            />
          </router-link>
        </figure>
      </div>
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
      destinations: store.destinations,
    };
  },
};
</script>
<style scoped>
.home {
  max-width: 1400px;
  margin: 0 auto;
}

img {
  max-width: 200px;
}

.destination {
  display: flex;
  justify-content: space-between;
}
</style>
