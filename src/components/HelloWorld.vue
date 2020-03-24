<template>
  <v-container>
    <v-row>
      <v-col>
        <table>
          <tbody>
            <tr v-for="(ligne,j) in ligne" :key="j">
              <td v-for="(colonne ,i) in colonne" :key="i">R{{j+1}}m{{i+1}}</td>
            </tr>
          </tbody>
        </table>
      </v-col>
    </v-row>
    <v-btn color="primary" @click="melanger">Melanger</v-btn>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    ligne:Number,
    colonne:Number
  },
  data: () => ({
    tableau:[]
  }),
  methods:{
    melanger(){
      let taille = this.ligne * this.colonne
      console.log(taille)
      for(let i=1; i< taille +1  ; i++){
        //let ligne = "R"++"M"+i
        console.log("R"+i+"M"+i)
      }
    }
  }
};
</script>

<style>
td {
  border: black solid 0.2em;
}
</style>
