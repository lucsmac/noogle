<template>
  <div id="app">
    <TheHeader />
    <SearchArea class="main" />
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
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
}

.main {
  flex: 1;
}
</style>
