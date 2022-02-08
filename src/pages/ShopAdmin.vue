<template>
  <section>
    <div v-if="isLoggedIn">
      <h2>Shop Admin</h2>
      <p>There isn't much to do at the moment - sorry ...</p>
    </div>
  </section>
</template>
<script>
export default {
  inject: ['isLoggedIn', 'login', 'logout'],
};
</script>

<style scoped>
section {
  text-align: center;
  margin: 3rem auto;
  max-width: 40rem;
  border: 1px solid #ccc;
  border-radius: 12px;
  padding: 2rem;
}
</style>
