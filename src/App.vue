<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <h4 class="d-flex align-center">Planification Experimentation</h4>
      <template v-slot:extension>
        <v-col cols="3">
          <v-text-field  v-model="ligne" label="Ligne" outlined></v-text-field>
        </v-col>
        <v-col cols="3">
          <v-text-field  v-model="colonne" label="Colonne" outlined></v-text-field>
        </v-col>
        <v-col>
          <v-btn @click="generate()">Generer</v-btn>
        </v-col>
      </template>
    </v-app-bar>

    <v-content>
      <HelloWorld :colonne="colonneSelected" :ligne="ligneSelected" class="tableau" />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld
  },

  data: () => ({
    ligne: null,
    colonne: null,
    ligneSelected:null,
    colonneSelected:null
  }),
  methods:{
    generate(){
      this.ligneSelected = parseInt(this.ligne)
      this.colonneSelected = parseInt(this.colonne)
    }
  }
};
</script>

<style >
.tableau {
  margin-top: 10em;
}
</style>
