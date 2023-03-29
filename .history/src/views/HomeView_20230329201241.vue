<template>
  <div class="home">
    <h1>All Desinations</h1>
    <div class="destinations">
      <div v-for="destination in destinaitons" :key="destination.name">
        <router-link :to="destination.slug">
          <h2>{{ destinaitons.name }}</h2>
        </router-link>
        <figure>
          <router-link :to="destinaiton.name">
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
      destinaitons: store.destinations,
    };
  },
};
</script>
<style scoped>
.home{
  max-width: 1400px;
  margin: 0 auto;
}
</style>