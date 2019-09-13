<template>
  <div id="app">
    <TheHeader />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";

export default {
  name: "app",
  components: {
    TheHeader
  }
};
</script>

<style lang="scss">
#app {
  margin: 0;
  padding: 0;
}
</style>
