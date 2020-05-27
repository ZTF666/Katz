<template>
 <v-layout >
    <v-flex xs12 sm6 offset-sm3 mt-10>
      <v-card>
        <v-img
          src="../assets/cat.jpg"
          aspect-ratio="2.75"
        ></v-img>

        <v-card-title primary-title class="text-md-center" >
          <div>
            <h3 class="headline mb-10 ">😻Random Fact😻</h3>
            <div> {{ card_text }} </div>
          </div>
        </v-card-title>

        <v-card-actions class="justify-center">
          <v-btn flat color="purple">😺Load Another😺</v-btn>
        </v-card-actions>

      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>


export default {
 data(){
   return {
      card_text: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.'
   }
 }
}
</script>
