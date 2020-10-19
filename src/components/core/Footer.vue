<template>
    <v-footer absolute height="60">
    <v-row justify="center" align="center" dense>
        <v-col cols="2" v-for="(tab, i) in tabs" :key="i">
            <router-link :to="tab.to">
                <v-btn icon>
                    <v-icon>
                        {{ tab.icon }}
                    </v-icon>
                </v-btn>
            </router-link>
        </v-col>
        <v-col cols="2">
            <router-link to="/">
                <v-btn icon>
                    <v-avatar size="30">
                        <v-img src="https://jmagazine.joins.com/_data/photo/2019/04/2949993301_QGcF14Px_1.jpg" alt="#"></v-img>
                    </v-avatar>
                </v-btn>
            </router-link>
        </v-col>
    </v-row>        
    </v-footer>
</template>

<script>
    export default {
        name:'Footer',
        data(){
            return {
                tabs: [
                    {
                        to: '/',
                        icon: 'mdi-home-variant'
                    },
                    {
                        to: '/',
                        icon: 'mdi-magnify'
                    },
                    {
                        to: '/',
                        icon: 'mdi-plus-box'
                    },
                    {
                        to: '/',
                        icon: 'mdi-heart-outline'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>