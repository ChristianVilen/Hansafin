<template>
  <v-container class="container">
    <AppHeader v-if="!isMobile"/>
    <AppMobileHeader v-else/>
    <nuxt/>
    <AppFooter/>
  </v-container>
</template>

<script>
import AppFooter from "~/components/AppFooter";
import AppHeader from "~/components/AppHeader";

export default {
  components: {AppHeader, AppFooter},
  mounted() {
    console.log(this.$vuetify.breakpoint.xsOnly)
  },
  computed: {
    isMobile() {
      return this.$vuetify.breakpoint.xsOnly;
    }
  }
};
</script>

<style>
@font-face {
  font-family: "Qanaya";
  src: local("Qanaya"),
  url(../assets/fonts/Qanaya-Regular-Demo.ttf), format("truetype");
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
</style>
