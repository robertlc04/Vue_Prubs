<template>
  <main>
    <section class="welcome_msg">
      <h1>Welcome to, <span class="highlight">Flashcards</span></h1>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ea, asperiores
        officiis dolore dicta velit mollitia totam dolorum doloremque nemo quae
        provident ratione! Culpa quod, voluptatibus provident saepe facere atque
        voluptas!
      </p>
    </section>
    <section class="features">
      <h2>App Features</h2>
      <article class="box_features">
        <FeaturesCards title="Organize your Ideas" />
        <FeaturesCards title="Control your Progress" />
        <FeaturesCards title="Maintain your Learning" />
      </article>
    </section>
  </main>
</template>

<script>
// @ is an alias to /src
import FeaturesCards from "@/components/home/FeaturesCards.vue";

export default {
  name: "HomeView",
  components: {
    FeaturesCards,
  },
};
</script>

<style scoped>
main {
  margin: 20px 0px;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}

@media (max-width: 768px) {
  main {
    flex-direction: column;
    place-items: center;
  }

  .box_features {
    flex-direction: column !important;
    place-items: center;
  }
  .welcome_msg {
    margin: 10px;
  }
}

.welcome_msg {
  max-width: 500px;
}

.box_features {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}

.highlight {
  color: var(--tertiary-color);
}
</style>
