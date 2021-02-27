<template>
  <v-app>
    <v-row class="holder">
      <v-col class="d-flex justify-center">
        <article id="main-col">
          <h1>Timo Vilèn</h1>
          <p>
            Yli 40 vuotta taloushallintoa ja liikkeenjohtoa, kotimaassa sekä kansainvälisesti (erityisesti Venäjän
            liiketoiminta kokemus). Ekonomi ja HT-tilintarkastustutkinto.
            Toimitusjohtajan ja talousjohtajaan tehtäviä pienissä ja isommissakin (konserni) yrityksissä.
          </p>
        </article>
      </v-col>
      <v-col class="d-flex justify-center">
        <aside id="sidebar">
          <div class="dark">
            <h3>Yhteystiedot</h3>
            <p>
              Timo Vilèn <br/>
              Minttutie 21 A<br/>
              Vantaa<br/>
              01300</p>
            <p>
              +358 400423282<br/>
              timo.vilen(at)mgiaudit.fi<br/>
              timo.vilen(at)elisanet.fi <br/>
              Y-tunnus: 1896646-0
            </p>
          </div>
        </aside>
      </v-col>
    </v-row>
    <AppForm />
  </v-app>
</template>

<script>
export default {
  name: "yhteystiedot",
  head() {
    return {
      title: "Yhteystiedot",
      meta: [
        {
          hid: "yhteystiedot",
          name: "yhteystiedot",
          content: "Tilintarkastus"
        }
      ]
    };
  },
};
</script>

<style scoped>
.holder {
  padding: 50px;
}
</style>
