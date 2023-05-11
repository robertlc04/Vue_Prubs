<template>
  <section class="card">
    <h1>{{ title }}</h1>
    <div class="content">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Recusandae vel
      aliquid sed tempore dignissimos molestiae nihil? Officia eaque, esse quos
      quaerat dolorem et laudantium ea cumque qui illum, modi sunt?
    </div>
  </section>
</template>

<script>
export default {
  name: "FeaturesCards",
  props: {
    title: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  width: 100%;
  max-width: 250px;
  margin: 20px;
  border-radius: 20px;
  padding: 20px;
  background-color: var(--background-secondary);

  h1 {
    color: var(--tertiary-color);
    font-size: 1.5rem;
  }

  .content {
    color: var(--primary-color);
  }
}
</style>
