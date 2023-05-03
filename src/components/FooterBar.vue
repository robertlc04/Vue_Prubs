<template>
  <section class="socials">
    <div class="socials-icons">
      <div class="twitter">
        <i class="bi bi-twitter"></i>
      </div>
      <div class="github">
        <i class="bi bi-github"></i>
      </div>
      <div class="reddit">
        <i class="bi bi-reddit"></i>
      </div>
    </div>

    <p>Copyrights 2023</p>
  </section>
</template>

<script></script>

<style lang="scss" scoped>
.socials {
  display: grid;
  width: 100%;
  height: 100px;
  max-height: 300px;
  background-color: rgba(70, 63, 58, 0.8);
  align-items: end;
}
.socials-icons {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;

  div {
    width: 3%;
    height: 50%;
    margin: 0 10px;
    border-radius: 50%;
    border-color: "#D9D9D9";
    border: 1px solid;
  }
}
</style>
