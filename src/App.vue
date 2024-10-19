<script>
  import  Header  from "./components/Header.vue"
  import StatsList from "./components/StatsList.vue";
  export default {
    components: { Header, StatsList }
  }
</script>

<template>
  <main className="main-page">
    <Header />
    <StatsList />
  </main>
</template>

<style scoped>
  .main-page {
    height: 1024px;
    background-color: rgb(53, 2, 79);
  }
</style>
