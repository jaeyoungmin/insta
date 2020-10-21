<template>
   <v-row class="icons-container" no-gutters>
       <v-btn icon><v-icon>mdi-heart-outline</v-icon></v-btn>
       <v-btn icon><v-icon>mdi-chat-outline</v-icon></v-btn>
       <v-btn icon><v-icon>mdi-send-outline</v-icon></v-btn>
       <v-spacer></v-spacer>
       <v-btn icon><v-icon>mdi-bookmark-outline</v-icon></v-btn>
   </v-row>
</template>

<script>
    export default {
        name: 'icons-container',
         data () {
      return {

     }
      }
    }
</script>

<style lang="scss" scoped>
.icons-container{
    width:100%;
    padding:16px;
}
</style>