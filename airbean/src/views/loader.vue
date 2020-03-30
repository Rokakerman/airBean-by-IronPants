<template>
  <article class="loading-container">
    <img src="../assets/graphics/loader.png" alt="loader" />
  </article>
</template>

<script>
export default {
  created() {
    setTimeout(() => this.$router.push('/status'), 4000)
  }
}
</script>

<style scoped>
.loading-container {
  width: 100vw;
  height: 100vh;
  margin: auto;
  background-color: #e5674e;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
