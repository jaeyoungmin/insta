<template>
  <div class="main">
    <story-slider />
    <post v-for="(post, i) in posts" :key="i" :post="post" :index="i"></post>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  name: 'Main',
  computed: { ...mapState(['posts']) },
  components: {
    StorySlider: () => import('@/components/main/StorySlider.vue'),
    Post: () => import('@/components/main/Post.vue'),
  },
};
</script>

<style lang="scss" scoped>
.main {
  padding-bottom: 50px;
}
</style>
