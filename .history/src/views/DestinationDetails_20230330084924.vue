<template>
  <section class="destination">
    <h1>{{ destination.name }}</h1>
    <div>
      <img :src="require(``)" :alt=""
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      destinationId: this.$route.params.id,
    };
  },
};
</script>
