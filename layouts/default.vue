<template>
  <v-app dark>
   <v-app-bar app color="dark" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          :src="logo"
          transition="scale-transition"
          width="40"
        />

        <v-text>Katz</v-text>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/ZTF666/Avatar-Fetcher"
        target="_blank"
        text
      >
        <span class="mr-2">Github Repo</span>
        <v-icon>mdi-github</v-icon>
      </v-btn>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      
    }
  }
}
</script>
