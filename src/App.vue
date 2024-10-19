<script>
  import  Header  from "./components/Header.vue"
  export default {
    components: { Header },
  }
</script>

<template>
  <main className="main-page">
    <Header />
  </main>
</template>

<style scoped>
  .main-page {
    height: 1024px;
    background-color: rgb(53, 2, 79);
  }
</style>
