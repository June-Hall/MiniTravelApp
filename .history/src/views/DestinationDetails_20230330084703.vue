<template>
  <p>The destination is {{ this.$route.params.id }}</p>
</template>

<script>
import destination

export default {
  data() {
    return {
      destinationId: this.$route.params.id,
    };
  },
};
</script>
