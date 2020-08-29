<template>
  <v-app class="yellow">
    <v-app-bar app color="grey " dark>
      <div class="d-flex align-center">
        

        
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
       
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
        <router-view></router-view>  
    </v-main>
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
