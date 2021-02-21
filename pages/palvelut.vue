<template>
  <v-app>
    <v-row class="holder">
      <v-col cols="12" class="d-flex justify-center title-holder">
        <h1>Palvelut</h1>
      </v-col>
      <v-col cols="6" sm="6" xl="3" class="paragraph">
        <article>
          Tilintarkastus on yhteisöjen kirjanpidon, tilipäätöksen ja hallinnon
          lakisääteistä varmennusta. Tilintarkastuksen avulla varmistamme, että
          asiakasorganisaatiomme johdon, omistajien ja muiden sidosryhmien saama
          taloudellinen tieto on luotettavaa. Meillä BDO:lla tilintarkastuksen
          kulmakivinä ovat laatu, riippumattomuus ja eettisyys. Toimintamme
          perustuu pitkäaikaisiin ja luottamuksellisiin asiakassuhteisiin sekä
          mutkattomaan henkilökohtaiseen kanssakäymiseen.
          Asiakastyytyväisyysmittauksemme* osoittaa, että 95 % asiakkaistamme on
          tyytyväisiä palveluihimme.
        </article>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  name: "palvelut",
  head() {
    return {
      title: "Palvelut",
      meta: [
        {
          hid: "palvelut",
          name: "palvelut",
          content: "Tilintarkastus palvelut"
        }
      ]
    };
  }
};
</script>

<style scoped>
.title-holder {
  padding: 20px;
}
.paragraph {
  margin: 0 auto;
}
.holder {
  height: 90vh;
  display: block;
  margin-top: 5vh;
  background-image: url("../assets/florian-klauer-mk7D-4UCfmg-unsplash.jpg");
  background-color: #cccccc; /* Used if the image is unavailable */
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
  background-size: cover; /* Resize the background image to cover the entire container */
}
</style>
