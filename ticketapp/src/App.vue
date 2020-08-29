<template>
  <v-app class="yellow">
    <v-app-bar 
    src="assets/cinemaBackground.png"
    app 
    
    color="grey darken-3" dense>
    
    <template v-slot:img="{ props }">
      <v-img
      v-bind="props"
      gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)"
      >

      </v-img>
    </template>

       
    <span class="white--text sub-title">Our cinema</span>
    <v-spacer></v-spacer>
    <v-btn text>Our Movies</v-btn>  
    </v-app-bar>

    <v-main>
        <router-view></router-view>  
    </v-main>

    <v-footer absolute>
      <v-card></v-card>
    </v-footer>
  </v-app>
</template>

<script>


export default {
  name: "App",

  components: {
    
  },

  data: () => ({
    //
  })
};
</script>
