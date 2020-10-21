<template>
  <div class="home">
    <div class="home-content">
      <core-App-bar class="core-app-bar" />
      <core-View class="core-view" />
      <core-footer class="core-footer" />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
    CoreAppBar: () => import('@/components/core/AppBar.vue'),
    CoreView: () => import('@/components/core/View.vue'),
    CoreFooter: () => import('@/components/core/Footer.vue'),
  },
};
</script>
<style lang="scss" scoped>
.home {
  background-color: #e7e7e7;
  display: flex;
  flex-flow: row;
  justify-content: center;
}
.home .home-content {
  width: 100%;
  max-width: 560px;
  min-height: 100vh;
  background-color: #fff;
  position: relative;
}
.core-footer {
  position: fixed;
  bottom: 0;
  max-width: 560px;
  margin: 0 auto;
}
</style>
