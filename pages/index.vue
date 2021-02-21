<template>
  <v-app>
    <v-row class="container">
      <v-col class="img-holder">
        <img
          src="../assets/hiking.svg"
          alt="Auditor at the park"
          height="500px"
          width="auto"
        />
      </v-col>
      <v-col>
        <h1>Tilintarkastus</h1>
        <article>
          <p>
            Tilintarkastuksella on useita erilaisia tehtäviä.
            Tilintarkastuksella varmistetaan niin tilinpäätöksen oikeellisuus,
            kuin osapuolien tasavertainen kohtelu ja laillisuus. Lisäksi
            tilintarkastuksen avulla luodaan luottamusta yhtiön sidosryhmille,
            jotta he voivat tehdä oikeisiin tietoihin perustuvia päätöksiä
            (kuten pankit ja sijoittajat).
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
  font-family: "Qanaya";
}

.img-holder {
  padding-top: 30px;
}
</style>
