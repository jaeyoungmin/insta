<template>
    <div class="image-card">
        <!-- <v-card v-for="(image, i) in stories" :key="i" elevation="1" class="image-card">
           <div class="profile-title d-flex">
               <v-btn icon>
                   <v-avatar>
                       <v-img :src="image.img" alt="#"/>
                   </v-avatar>
               </v-btn>
               <p>{{image.name}}</p> 
               <v-spacer></v-spacer>
               <v-btn icon>
                   <v-icon>
                       mdi-dots-horizontal
                   </v-icon>
               </v-btn>
            </div>
            <div class="image-box">
                <v-img :src="image.img" :aspect-ratio="1/1"></v-img>
            </div>
            <div class="d-flex">
                <v-btn icon>
                    <v-icon>mdi-heart-outline</v-icon>
                </v-btn>
                <v-btn icon>
                    <v-icon>mdi-chat-outline</v-icon>
                </v-btn>
                <v-btn icon>
                    <v-icon>mdi-send-outline</v-icon>
                </v-btn>
            </div>
        </v-card> -->
      
    </div>
</template>

<script>
import {mapState} from 'vuex';
    export default {
        name: 'ImageCard',
        computed: { ...mapState(["stories", "post"]) }
    }
</script>

<style lang="scss" scoped>
.profile-title{
    padding:10px 13px;
    img{
        object-fit: cover;
    }
    p{
        margin: 5px 0 0 20px;
    }
}
.image-card{
    margin-bottom:15px;
}
</style> 