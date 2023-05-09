<template>
  <main>
    <h1>Application Basics Functionality</h1>
    <section class="cards">
      <CardsModel title="Create Flashcards" btn_name="Enter" />
      <CardsModel
        title="Create Model"
        icon_name="bi-card-text"
        btn_name="Enter"
      />
      <CardsModel title="Create Deck" icon_name="bi-archive" btn_name="Enter" />
      <CardsModel title="Modify Flashcards" btn_name="Enter" />
      <CardsModel
        title="Modify Model"
        icon_name="bi-card-text"
        btn_name="Enter"
      />
      <CardsModel title="Modify Deck" icon_name="bi-archive" btn_name="Enter" />
    </section>
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
  margin: 5% auto 10%;
  z-index: 99;

  .cards {
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    margin-bottom: 1%;
  }

  h1 {
    color: var(--primary-color);
  }
}
</style>
