<template>
  <div id="app">
    <IMCCard />
  </div>
</template>

<script>
import IMCCard from './components/Container/IMCCard/IMCCard.vue';

export default {
  name: 'App',
  components: {
    IMCCard,
}
}
</script>

<style lang="scss">
html {
  background-color: rgba(245, 197, 78, 0.6);
}

#app {
  text-align: center;
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

</style>
