<template>
  <p>The destination is {{ this.$route.params.id }}</p>
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
