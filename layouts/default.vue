<template>
  <v-container class="container">
    <AppHeader />
    <nuxt />
    <AppFooter />
  </v-container>
</template>

<script>
import AppFooter from "~/components/AppFooter";
import AppHeader from "~/components/AppHeader";

export default {
  components: { AppHeader, AppFooter },
  data() {
    return {};
  }
};
</script>
<style scoped lang="scss"></style>

<style>
@font-face {
  font-family: "Qanaya";
  src: local("Qanaya"),
  url(../assets/Qanaya-Regular-Demo.ttf), format("truetype");
}
body {
  font-family: "Qanaya", Arial, Helvetica, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  height: 100%;
}

.container {
  min-height: 100%;
}

.call-to-action {
  height: 50px;
  margin-top: -50px;
}
</style>
