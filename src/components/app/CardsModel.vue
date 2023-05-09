<template>
  <section class="conteiner">
    <div class="circle"><i :class="iname"></i></div>
    <main class="content">
      <h1>{{ title }}</h1>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempore nulla
      iure magnam libero at fugiat, ullam sapiente veritatis alias minima.
      Commodi nihil quaerat nulla aspernatur deserunt repudiandae eveniet
      exercitationem maiores! Lorem, ipsum dolor sit amet consectetur
      adipisicing elit. Eos quae blanditiis id recusandae, dolorum natus rem
      nihil dolor placeat! Deserunt pariatur perferendis aliquid corporis
      corrupti doloremque veniam provident asperiores et.
    </main>
    <button class="btn btn-secondary service">{{ btn_name }}</button>
  </section>
</template>

<script lang="js">
export default {
  props: {
  	title: String,
    icon_name: String,
    btn_name: String
  },
  data () {
    return {
      iname: ''
    }
  },
  methods: {
    change_style () {
      if (this.icon_name !== '' && this.icon_name !== undefined) {
        this.iname = `bi ${this.icon_name}`
      } else {
        this.iname = 'bi bi-plus'
      }
    }
  },
  mounted () {
    this.change_style()
  }

}
</script>

<style lang="scss" scoped>
.conteiner {
  width: 100%;
  height: 100%;
  max-width: 300px;
  margin: 3%;

  border-radius: 10px;
}

.content {
  background: #ccc;
  border-radius: 10px;
  padding: 20px;

  h1 {
    font-size: 25px;
  }
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

.service {
  position: relative;
  top: -20px;
  background-color: var(--background-secondary);
  border-radius: 10px;
  padding: 5px 30px;
  font-size: 15px;
  color: var(--tertiary-color);
  font-style: to-upper-case;
  border: none;

  :hover {
    border: 1px solid var(--tertiary-color);
    transition: 0.5s;
  }
}
</style>
