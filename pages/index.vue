<template>
 <v-layout >
    <v-flex xs12 sm6 offset-sm3 mt-10>
      <v-card>
        <v-img
          :src="src"
        aspect-ratio="2.75"
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
     src:'',
      card_text: '',
       katz:['https://firebasestorage.googleapis.com/v0/b/katzfacts.appspot.com/o/2.png?alt=media&token=09a93a8e-babc-4944-9a7d-5c466a4c1db7',
    'https://firebasestorage.googleapis.com/v0/b/katzfacts.appspot.com/o/7.png?alt=media&token=e6baf0b6-5e15-4a09-98c4-60e976c9045f',
    'https://firebasestorage.googleapis.com/v0/b/katzfacts.appspot.com/o/6.png?alt=media&token=43b20b5f-1a93-4e5a-a047-c20c7cd6ae20',
    'https://firebasestorage.googleapis.com/v0/b/katzfacts.appspot.com/o/5.png?alt=media&token=32864c11-38c4-4f5b-a724-295d69685c8f',
    'https://firebasestorage.googleapis.com/v0/b/katzfacts.appspot.com/o/4.png?alt=media&token=45d1766b-e5dd-43d3-9512-12de11351db8',
    'https://firebasestorage.googleapis.com/v0/b/katzfacts.appspot.com/o/3.png?alt=media&token=3bb06176-6bad-40f3-8f8a-363b51b9372f',
    'https://firebasestorage.googleapis.com/v0/b/katzfacts.appspot.com/o/8.png?alt=media&token=aea64efe-3f91-4aea-9c44-fc4781705bbf',
    'https://firebasestorage.googleapis.com/v0/b/katzfacts.appspot.com/o/1.png?alt=media&token=a784344e-e951-4a09-a4c1-fc6d8be284f3']
   }
 },
  methods:{
    async loadFacts(){
      let response = await axios.get('https://catfact.ninja/fact')
      this.card_text = response.data.fact
      this.src=this.katz[Math.floor(Math.random() * this.katz.length)]




    }
  },
  mounted(){
    this.loadFacts()
  }
}
</script>
