<template>
  <article class="loading-container">
    <img src="../assets/graphics/loader.png" alt="loader" />
  </article>
</template>

<script>
export default {
  created() {
    setTimeout(() => this.$router.push('/status'), 5000)
  }
}
</script>

<style scoped>
.loading-container {
  width: 100vw;
  height: 100vh;
  margin: auto;
  background-color: #2f2926;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
