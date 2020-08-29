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
            
            
          </v-col>
        </v-row>
      </v-container>
    </v-img>

    <v-container class="black lighten-2" fluid>
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
              
              <p></p>
              <p></p>
              <p></p>
            </v-flex>
            
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
            
            <v-flex class="mx-2 white--text font-weight-bold headline">
              <p class="">Unhinged</p>
            </v-flex>

            
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
            
            <v-flex class="mx-2 white--text font-weight-bold headline">
              Contagion
            </v-flex>

            
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
  }
};
</script>
