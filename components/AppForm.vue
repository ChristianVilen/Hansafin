<template>
<section>
  <v-row>
      <v-col cols="12" class="d-flex justify-center">
        <img
          src="../assets/svg/option.svg"
          alt="alt text"
          height="100px"
          width="auto"
        />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="d-flex justify-center" v-if="!showAlert">
        <h3>
          Ota yhteyttä!
        </h3>
      </v-col>
      <v-col v-else class="d-flex justify-center">
        <v-alert dense type="success">
          Kiitos yhteydenotosta! Vastaamme viestiinne mahdollisimman pian.
        </v-alert>
      </v-col>
    </v-row>
    <v-row class="d-flex justify-center">
      <v-col cols="8" sm="6">
        <v-form v-model="valid" @submit.prevent="onSubmit" @reset="onReset">
          <v-text-field
            v-model="form.name"
            :rules="nameRules"
            label="Nimi"
            required
          ></v-text-field>

          <v-text-field
            v-model="form.email"
            :rules="emailRules"
            label="Sähköposti"
            required
          ></v-text-field>

          <v-textarea
            outlined
            auto-grow
            v-model="form.message"
            label="Viesti"
            required
          ></v-textarea>

          <v-btn color="success" :disabled="!valid" type="submit">
            Lähetä
          </v-btn>
          <p v-if="fail" style="color: red">Jotain meni väärin</p>
        </v-form>
      </v-col>
    </v-row>
</section>
</template>

<script>
import axios from "axios";

export default {
  name: "AppForm",
  data() {
    return {
      valid: false,
      fail: false,
      showAlert: false,
      form: {
        name: "",
        email: "",
        message: ""
      },
      nameRules: [v => !!v || "Lisää nimi"],
      emailRules: [
        v => !!v || "Lisää sähköposti",
        v => /.+@.+/.test(v) || "Tarkista sähköposti"
      ]
    };
  },
  methods: {
    onSubmit() {
      axios
        .post("https://formspree.io/f/xleokvdg", this.form)
        .then(() => {
          this.showAlert = true
          this.onReset()
        })
        .catch(() => (this.fail = true));
    },
    onReset() {
      this.form.name = "";
      this.form.email = "";
      this.form.message = "";
    }
  }
}
</script>

<style scoped>

</style>
