<template>
  <section>
    <h1>Experiences</h1>
    <h2>{{ experience.name }}</h2>
    <div class="experience-details">
      <img
        :src="require(`@/assets/$experience.image`)"
        :alt="experience.name"
      />
      <p>{{ experience.name }}</p>
    </div>
  </section>
</template>
