<template>
    <span>
        <v-card class="">
            <v-card-title>
                <span class="headline">Sign in</span>
            </v-card-title>
            <v-card-text>
                <v-container>
                    <v-row>
                        <v-col cols="6">
                            <v-text-field label="First Name" ></v-text-field>
                        </v-col>
                        <v-col cols="6">
                            <v-text-field label="Last Name" ></v-text-field>
                        </v-col>
                        <v-col cols="4">
                            <v-text-field label="Username" ></v-text-field>
                        </v-col>
                        <v-col cols="4">
                            <v-text-field label="Password" type="password" ></v-text-field>
                        </v-col>
                        <v-col cols="4">
                            <v-text-field label="Age" type="number" min="15" max="100"></v-text-field>
                        </v-col>
                    </v-row>
                </v-container>
            </v-card-text>
            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn class="" text @click="$emit('closeDialog')">Cancel</v-btn>
                <v-btn text @click="$emit('closeDialog')">Save</v-btn>
            </v-card-actions>
        </v-card>
        
    </span>
</template>
<script>
    export default{
        data:()=>{
            return{
                dialog:true
            }
        },
        methods:{
            CloseDialog(){
                console.log("Hello")
                this.$emit('closeDialog')
            }
        }
    }
</script>