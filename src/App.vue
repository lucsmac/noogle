<template>
  <div id="app">
    <TheHeader />
    <SearchArea />
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import SearchArea from "./components/SearchArea.vue";

export default {
  name: "app",
  components: {
    TheHeader,
    TheFooter,
    SearchArea
  },
  created() {
    document.title = "Noogle";
  }
};
</script>

<style lang="scss">
#app,
body {
  margin: 0;
  padding: 0;
  min-width: 100vh;
}

.main {
  flex: 1;
}
</style>
