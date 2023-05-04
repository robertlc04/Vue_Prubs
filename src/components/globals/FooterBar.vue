<template>
  <section class="socials">
    <div class="socials-icons">
      <div class="twitter">
        <a href="#"><i class="bi bi-twitter"></i></a>
      </div>
      <div class="github">
        <a href="#"><i class="bi bi-github"></i></a>
      </div>
      <div class="reddit">
        <a href="#"><i class="bi bi-reddit"></i></a>
      </div>
    </div>

    <p>Copyrights 2023</p>
  </section>
</template>

<script></script>

<style lang="scss" scoped>
.socials {
  margin-top: 5px;
  display: grid;
  grid-template-rows: 5fr 1fr;
  width: 100%;
  height: 100px;
  max-height: 300px;
  background-color: rgba(70, 63, 58, 0.8);
  align-items: end;

  p {
    margin-bottom: 10px;
  }
}
.socials-icons {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: end;

  div {
    width: 3%;
    height: 50%;
    margin: 0 10px;

    a {
      color: black;
      text-decoration: none;
      i {
        font-size: 24px;
      }
    }
  }
}
</style>
