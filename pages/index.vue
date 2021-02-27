<template>
  <v-app>
    <v-row class="container">
      <v-col cols="12" sm="6" class="img-holder">
        <img
          class="img"
          src="../assets/svg/hiking.svg"
          alt="Auditor at the park"
        />
      </v-col>
      <v-col>
        <h1>Hansafin Oy</h1>
        <article>
          <p>
            on vantaalainen yritysjohdon ja taloushallinnon konsulttiyhtiö, jonka päätoimiala on
            tilintarkastuspalvelut, joiden toteutus tapahtuu
            osakkuusyhtiö MGI Tilintarkastus Oy:n kautta, kts www.mgiaudit.fi.
          </p>
        </article>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  components: {},
  head() {
    return {
      title: "Hansafin",
      meta: [
        {
          hid: "etusivu",
          name: "etusivu",
          content: "Hansafin tilintarkastus"
        }
      ]
    };
  }
};
</script>

<style scoped lang="scss">
h1 {
  font-family: "Qanaya", serif;
}

.img-holder {
  padding-top: 30px;
}

.img {
  height: 500px;
  width: auto;
}

@media only screen and (max-width: 678px) {
  .img-holder {
    overflow-x: hidden;
  }
}
</style>
