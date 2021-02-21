<template>
  <div>
    <v-app-bar color="deep-purple accent-4" dense>
      <v-col cols="4">
        <v-toolbar-title><h2>Hansafin</h2></v-toolbar-title>
      </v-col>

      <v-tabs class="nav-bar">
        <v-tab><nuxt-link class="link" to="/">Etusivu</nuxt-link></v-tab>
        <v-tab
          ><nuxt-link class="link" to="/palvelut">Palvelut</nuxt-link></v-tab
        >
        <v-tab
          ><nuxt-link class="link" to="/yhteystiedot"
            >Yhteystiedot</nuxt-link
          ></v-tab
        >
      </v-tabs>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "AppHeader"
};
</script>

<style lang="scss" scoped>
* {
  font-family: "Qanaya";
}
.link {
  text-decoration: none;
  color: black;
}
</style>
