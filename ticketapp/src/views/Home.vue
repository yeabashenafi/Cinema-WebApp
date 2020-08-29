<template>
  <span>
    <v-img
    :src="require('../assets/focus-3.jpg')"
    aspeect-ratio="2"
    >
      <v-container fill-height>
        <v-row justify="center" align="center">
          <v-col class="white--text" cols="7">
            <p class="mx-12 display-3 cyan--text font-weight-bold"> Our cinema</p>
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
                <v-btn flat @click="$vuetify.goTo($refs.movies,options)">See our latest Movies</v-btn>
              </v-row>
            </v-container>
            
            
            
          </v-col>
        </v-row>
      </v-container>
    </v-img>

    <v-container  fluid class="black" ref="movies">
      <v-row  
      justify="space-between"
      >
        <v-col cols='4' 
        v-for="(movie,index) in Movies"
        :key="index"
        >
          <v-card color="grey darken-4">
            <v-row no-gutters>
              <v-col cols="10">
                <v-img
                :src="require('../assets/' + movie.image)"
                aspect-ratio="0.7"
                >
                </v-img>
              </v-col>
              <v-col cols="2">
                <v-container fill-height>
                  <v-row align="center">
                    <v-col>
                      <v-icon large 
                      @click="likeMovie(index)"
                      :color="movie.liked ? 'red' :'white'" class="my-2">mdi-heart</v-icon>
                      <v-icon large 
                      @click="addMovie(index)"
                      :color="movie.inWishlist ? 'blue darken-2':'white'" class="my-2">mdi-bookmark</v-icon>
                      <p class="white--text">75Br.</p>
                    </v-col>
                  </v-row>
                </v-container>
              </v-col>
            </v-row>
            
            <v-flex class="mx-2 white--text ">
              <p class="font-weight-bold headline">{{movie.title}}</p>
              <v-container class="grey--text" fluid>
                <v-row justify="space-between ">
                  <v-col>{{movie.duration}}</v-col>
                  <v-col>{{movie.genre}}</v-col>
                  
                </v-row>
                <p>{{movie.description}}  
                </p>
                <v-flex class="text-center">
                  <p class="font-weight-bold cyan--text title">{{movie.time}}</p>
                </v-flex>
                
              </v-container>
            </v-flex>
            <v-card-actions class="my-10 text-center">
              <v-flex class="text-center">
                <v-btn @click="signinDialog = true">Buy Ticket</v-btn>
              </v-flex>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <v-dialog 
    v-model="signinDialog" 
    color="white" width="500" 
    persistent overlay-opacity="0.8">
      <signin-dialog @closeDialog="signinDialog = false"></signin-dialog>
    </v-dialog >

    <v-dialog v-model="likeDialog"
    width="500"
    persistent
    overlay-opacity="0.8"
    >
      <Success-dialog 
      @closeSuccess="likeDialog = false"
      :type="message" :name="movieName"></Success-dialog>
    </v-dialog> 
    
    <v-dialog 
    width="500"
    persistent
    v-model="wishDialog"
    overlay-opacity="0.8">
      <Success-dialog 
      @closeSuccess="wishDialog = false"
      :type="message" :name="movieName"></Success-dialog>
    </v-dialog>
  </span>        
</template>

<script>
// @ is an alias to /src
import SuccessDialog from "@/components/SuccessDialog.vue";
import signinDialog from "@/components/signinDialog.vue"
export default {
  name: "Home",
  components: {
    // HelloWorld
    signinDialog,
    SuccessDialog
  },
  data(){
    return{
      signinDialog:false,
      likeDialog:false,
      wishDialog:false,
      message:"",
      movieName:"",
      Movies:[
        {
          title:"Project Power",
          duration:"1h54min",
          liked:false,
          inWishlist:false,
          genre:"Action,Crime,Thriller",
          description:"A former soldier teams up with a cop to find the source behind a dangerous pill that provides superpowers.",
          image:'ppower.png',
          time:"Today 8pm ET"
        },
        {
          title:"Unhinged",
          duration:"1h30min",
          liked:false,
          inWishlist:false,
          genre:"Thriller,Mystery",
          description:"Unhinged is a 2020 American thriller film directed by Derrick Borte, from a screenplay by Carl Ellsworth.",
          image:'unhinged3.jpg',
          time:"Tommorow 5pm ET",
        },
        {
          title:'Contagion',
          duration:"1h46m",
          liked:false,
          inWishlist:false,
          genre:'Thriller,Drama',
          description:'The death of Beth Emhoff and her son leads to the discovery of a deadly virus. A worldwide panic ensues',
          image:"contagion3.jpg",
          time:"Today 5pm ET"
        }
      ],
      options:{
          duration: 300,
          offset: 0,
          easing: 'easeInOutCubic',
      }
    }
    
  },
  methods:{
      likeMovie(index){
        this.Movies[index].liked = !this.Movies[index].liked
        if(this.Movies[index].liked){
          this.likeDialog = true
          this.message = "Liked"
          this.movieName = this.Movies[index].title
        }
        
      },
      addMovie(index){
        this.Movies[index].inWishlist = !this.Movies[index].inWishlist
        if(this.Movies[index].inWishlist){
          this.wishDialog = true
          this.message = "Wishlist"
          this.movieName = this.Movies[index].title
        }
        
        // this.likeDialog = true
      }
    }
}
</script>
