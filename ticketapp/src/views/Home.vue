<template>
  <span>
    <v-img
    :src="require('../assets/focus-3.jpg')"
    aspeect-ratio="0.9"
    >
      <v-container fill-height>
        <v-row justify="center" align="center">
          <v-col class="white--text" cols="7">
            <p class="mx-12 display-4 cyan--text font-weight-bold"> Our cinema</p>
            <p class="mx-8 font-weight-bold">
              Lorem ipsum dolor sit amet, 
            consectetur adipiscing elit, sed do eiusmod tempor 
            incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, 
            quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
            Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat
             nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui 
             officia deserunt mollit anim id est laborum.
            </p>
            <v-container fill-height class="mt-16">
              <v-row align="space-around" justify="center">
                <v-btn @click="$vuetify.goTo($refs.movies,options)">See our latest Movies</v-btn>
              </v-row>
            </v-container>
            
            
            
          </v-col>
        </v-row>
      </v-container>
    </v-img>

    <v-container class="black lighten-2" fluid ref="movies">
      <v-row justify="space-between">
        <v-col cols='4' >
          <v-card color="grey darken-4">
            <v-row no-gutters>
              <v-col cols="10">
                <v-img
                :src="require('../assets/ppower.png')"
                aspect-ratio="0.7"
                >
                </v-img>
              </v-col>
              <v-col cols="2">
                <v-container fill-height>
                  <v-row align="center">
                    <v-col>
                      <v-icon large color="white" class="my-2">mdi-heart</v-icon>
                      <v-icon large color="white" class="my-2">mdi-bookmark</v-icon>
                      <p class="white--text">75Br.</p>
                    </v-col>
                  </v-row>
                </v-container>
              </v-col>
            </v-row>
            
            <v-flex class="mx-2 white--text ">
              <p class="font-weight-bold headline">Project Power</p>
              <v-container class="grey--text" fluid>
                <v-row justify="space-between ">
                  <v-col>1h54min</v-col>
                  <v-col>Action,Crime,Thriller</v-col>
                  
                </v-row>
                <p>  A former soldier teams 
                  up with a cop to find the source behind a 
                  dangerous pill that provides temporary superpowers.
                </p>
              </v-container>
            </v-flex>
            <v-card-actions class="my-10 text-center">
              <v-flex class="text-center">
                <v-btn>Buy Ticket</v-btn>
              </v-flex>
            </v-card-actions>
          </v-card>
        </v-col>

        <v-col cols='4' >
          <v-card color="grey darken-4">
            <v-row no-gutters>
              <v-col cols="10">
                <v-img
                :src="require('../assets/unhinged3.jpg')"
                aspect-ratio="0.7"
                ></v-img>
              </v-col>
              <v-col cols="2">
                <v-container fill-height>
                  <v-row align="center">
                    <v-col>
                      <v-icon large color="white" class="my-2">mdi-heart</v-icon>
                      <v-icon large color="white" class="my-2">mdi-bookmark</v-icon>
                      <p class="white--text">55Br.</p>
                    </v-col>
                  </v-row>
                </v-container>
              </v-col>
            </v-row>
            
            <v-flex class="mx-2 white--text ">
              <p class="font-weight-bold headline">Unhinged</p>
              <v-container class="grey--text " fluid>
                <v-row jsutify="space-between">
                  <v-col>1h30m</v-col>
                  <v-col>Thriller,Mystery</v-col>
                  
                </v-row>
                <p>
                  Unhinged is a 2020 American thriller film directed by Derrick Borte, from a screenplay by Carl Ellsworth. 
                </p>
              </v-container>
            </v-flex>
            <v-card-actions class="my-10 text-center">
              <v-flex class="text-center">
                <v-btn>Buy Ticket</v-btn>
              </v-flex>
              
            </v-card-actions>
            
          </v-card>
        </v-col>
        <v-col cols='4' >
          <v-card color="grey darken-4">
            <v-row no-gutters>
              <v-col cols="10">
                <v-img
                :src="require('../assets/contagion3.jpg')"
                aspect-ratio="0.7 "
                ></v-img>
              </v-col>
              <v-col cols="2" >
                <v-container fill-height>
                  <v-row align="center">
                    <v-col>
                      <v-icon large color="white" class="my-2">mdi-heart</v-icon>
                      <v-icon large color="white" class="my-2">mdi-bookmark</v-icon>
                      <p class="white--text">80Br.</p>
                    </v-col>
                  </v-row>
                </v-container>
                
                
                
              </v-col>
            </v-row>
            
            <v-flex class="mx-2 white--text ">
              <p class="font-weight-bold headline">Contagion</p>
              <v-container class="grey--text " fluid>
                <v-row jsutify="space-between">
                  <v-col>1h46m</v-col>
                  <v-col>Thriller,Drama</v-col>
                  
                </v-row>
                <p>The death of Beth Emhoff and her son leads to the discovery of a deadly virus. A worldwide panic ensues</p>
              </v-container>
            </v-flex>
            <v-card-actions class="my-10">
              <v-flex class="text-center">
                <v-btn>Buy Ticket</v-btn>
              </v-flex>
              
            </v-card-actions>
            
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </span>        
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld
  },
  data(){
    return{
      options:{
          duration: 300,
          offset: 0,
          easing: 'easeInOutCubic',
      }
    }
  }
};
</script>
