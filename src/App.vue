<template>
  <v-app>
    <router-view></router-view>
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
<style lang="scss">
    a{
        text-decoration: none;
    }
    *{
      box-sizing: border-box;
    }
    p{
      margin:0;
      padding: 0;
    }

</style>