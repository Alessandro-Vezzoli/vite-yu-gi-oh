<template>
  <AppHeader></AppHeader>
  <div class="background">
    <AppMain></AppMain>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
export default {
  name: "App",
  components: { AppHeader, AppMain },
};
</script>

<style scoped>
.background {
  background-color: orange;
}
</style>
