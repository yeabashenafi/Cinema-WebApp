<template>
    <span>
        <v-card>
            <v-card-text >
                <v-flex class="text-center title">
                    <p v-if="type == 'Liked'">
                        You have liked the movie {{name}}.
                    </p>
                    <p v-if="type == 'Wishlist'">
                        You have added the movie {{name}} to your wishlist.
                    </p>
                </v-flex>
                
            </v-card-text>
            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn @click="$emit('closeSuccess')">Ok</v-btn>
            </v-card-actions>
        </v-card>
    </span>
</template>
<script>
export default {
    props:{
        type:{
            type:String
        },
        name:{
            type:String
        }
    },
        
    
    data(){

    }

}
</script>