<template>
  <main>
    <h1>Application Basics Functionality</h1>
    <CardsModel />
  </main>
</template>
<script>
import CardsModel from "../components/app/CardsModel";
export default {
  components: {
    CardsModel,
  },
};
</script>
<style lang="scss" scoped>
main {
  margin: 5% auto;

  h1 {
    color: var(--primary-color);
  }
}
</style>
