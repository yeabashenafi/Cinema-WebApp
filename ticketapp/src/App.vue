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

       
    <span class="white--text title">Our cinema</span>
    <v-spacer></v-spacer>
    <!-- <v-btn text >Our Movies</v-btn>   -->
    </v-app-bar>

    <v-main>
        <router-view></router-view>  
    </v-main>

    
      <v-card color="grey lighten-2" width="100%" flat>
        <v-container fluid fill-height>
          <v-row class="mx-10" justify="center">
            <v-col>
              <p class="title">Information</p>
              <p class="mt-10 grey--text">About us</p>
              <p class="grey--text">Partners</p>
              <p class="grey--text">Events</p>
              <p class="grey--text">Partners</p>
            </v-col>
            <v-col>
              <p class="title">Contact us</p>
              <p class="mt-10 grey--text">Facebook</p>
              <p class="grey--text">E-mail</p>
              <p class="grey--text">Linked in</p>
              <p class="grey--text">Telegram</p>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    <!-- </v-footer> -->
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
