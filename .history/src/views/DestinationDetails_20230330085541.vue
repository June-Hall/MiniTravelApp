<template>
  <section class="destination">
    <h1>{{ destination.name }}</h1>
    <div class="destination-details">
      <img
        :src="require(`@/assets/$destination.image`)"
        :alt="destination.name"
      />
    </div>
  </section>
</template>

<script>
import store from "@/store";
export default {
  data() {
    return {
      destinationId: this.$route.params.id,
    };
  },
  computed() {
    return store.destinations.find(
      (destination) => destination.id === this.destinationId
    );
  },
};
</script>

<style scoped>
img {
  height: auto;
  width: 100%;
  max-height: 400px;
  max-width: 600px;
}

destination {
  
}
</style>
