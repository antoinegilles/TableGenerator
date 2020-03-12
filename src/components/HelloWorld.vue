<template>
  <v-container>
    <v-row>
      <v-col>
        <table>
          <tbody>
            <tr v-for="(colonne,j) in colonne" :key="j">
              <td v-for="(ligne,i) in ligne" :key="i">R{{j+1}}m{{i+1}}</td>
            </tr>
          </tbody>
        </table>
      </v-col>
    </v-row>
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
  })
};
</script>

<style>
td {
  border: black solid 0.2em;
}
</style>
