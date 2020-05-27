<template>
 <v-layout >
    <v-flex xs12 sm6 offset-sm3 mt-10>
      <v-card>
        <v-img
          :src="src"
       
        ></v-img>

        <v-card-title primary-title class="justify-center">
          <div>
            <h3 class="headline mb-10 ">😻Random Fact😻</h3>
          </div>
        </v-card-title>
        <v-card-text>
          <div ><h4 class="headline text-md-center"> {{ card_text }}</h4> </div>
        </v-card-text>

        <v-card-actions class="justify-center">
          <v-btn  color="purple" @click.prevent="loadFacts()">😺Load Another😺</v-btn>
        </v-card-actions>

      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import axios from 'axios'
export default {
 data(){
   return {
     src:require('../assets/cat.jpg'),
      card_text: ''
   }
 },
  methods:{
    async loadFacts(){
      let response = await axios.get('https://catfact.ninja/fact')
      this.card_text = response.data.fact
    }
  },
  mounted(){
    this.loadFacts()
  }
}
</script>
