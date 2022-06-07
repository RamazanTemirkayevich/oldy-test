<template>
  <Cards/>
</template>

<script>
import Cards from './components/Cards.vue'
export default {
  name: 'App',
  components: {
    Cards
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

body {
  margin: 0;
  padding: 0;
}

* {
  margin: 0;
  padding: 0;
}
</style>
