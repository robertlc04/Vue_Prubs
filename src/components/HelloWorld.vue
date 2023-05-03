<template>
  <div>
    <h1>{{ count }}</h1>
    <button class="btn btn-secondary" @click="increment">
      <i class="bi-plus-lg"></i>
      Increment
    </button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      count: 1
    }
  },

  methods: {
    increment () {
      this.count++
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
