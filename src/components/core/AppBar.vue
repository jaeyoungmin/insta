<template>
    <div class="v-app-bar" color="white">
 <v-app-bar color="white" elevation="1" >
    <router-link to="/">
        <v-btn icon color="#222">
            <v-icon>
                mdi-instagram
            </v-icon>
        </v-btn>
    </router-link>
    <v-spacer></v-spacer>
        <v-img class="logo" src="https://www.instagram.com/static/images/web/mobile_nav_type_logo.png/735145cfe0a4.png" max-width="120" alt="#"></v-img>
    <v-spacer></v-spacer>
    <router-link to="/">
        <v-btn icon color="#222">
            <v-icon>
                mdi-heart-outline
            </v-icon>
        </v-btn>
    </router-link>
 </v-app-bar>

    </div>
</template>

<script>
    export default {
        name: 'AppBar'
    }
</script>

<style lang="scss" scoped>

</style>