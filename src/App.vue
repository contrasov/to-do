<template>
  <MenuHeader/>
</template>

<script>
import MenuHeader from './components/MenuHeader.vue';

export default {
  name: 'App',
  components: {
    MenuHeader
  }
}
</script>

<style>
#app {
  font-family: 'Inter', sans-serif;
  text-align: center;
}

body {
  background-color: #101010;
}
</style>