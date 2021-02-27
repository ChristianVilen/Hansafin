<template>
  <v-card
    class="mx-auto overflow-hidden"
    :height="drawer ? 200 : 50"
  >
    <v-app-bar
      color="deep-purple"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>Hansafin</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>
              <nuxt-link class="link" to="/">Etusivu</nuxt-link>
            </v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>
              <nuxt-link class="link" to="/palvelut">Palvelut</nuxt-link>
            </v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>
              <nuxt-link class="link" to="/yhteystiedot">Yhteystiedot</nuxt-link>
            </v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>

<script>
export default {
  name: "AppMobileHeader",
  data() {
    return {
      drawer: false,
      group: null,
    }
  }
}
</script>

<style scoped>
* {
  font-family: "Qanaya",serif;
}

.link {
  text-decoration: none;
  color: black;
}
</style>
