<template>
  <section class="conteiner">
    <div class="circle"><i class="bi bi-plus"></i></div>
    <main class="content">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempore nulla
      iure magnam libero at fugiat, ullam sapiente veritatis alias minima.
      Commodi nihil quaerat nulla aspernatur deserunt repudiandae eveniet
      exercitationem maiores! Lorem, ipsum dolor sit amet consectetur
      adipisicing elit. Eos quae blanditiis id recusandae, dolorum natus rem
      nihil dolor placeat! Deserunt pariatur perferendis aliquid corporis
      corrupti doloremque veniam provident asperiores et.
    </main>
  </section>
</template>

<style lang="scss" scoped>
.conteiner {
  width: 100%;
  height: 100%;
  max-width: 270px;
  max-height: 300px;
  margin: 5%;

  border-radius: 10px;
}

.content {
  background: #ccc;
  border-radius: 10px;
  padding: 10px;
  padding-top: 20px;
}

.circle {
  position: relative;
  bottom: -15px;
  left: 40%;

  width: 16%;
  background-color: var(--background-primary);
  border-radius: 50%;

  i {
    width: 100%;
    height: 100%;
    margin: auto 0;
    font-size: 26px;
  }
}
</style>
