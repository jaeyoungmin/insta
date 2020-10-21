<template>
  <div class="post-component">
    <v-row class="post-head" align="center" no-gutters>
      <v-avatar size="40" class="head-avatar">
        <v-img :src="post.userProfile.img" alt="imag"></v-img>
      </v-avatar>
      <h3>{{ post.userProfile.name }}</h3>
      <v-spacer></v-spacer>
      <v-btn x-large icon><v-icon>mdi-dots-horizontal</v-icon></v-btn>
    </v-row>
    <!-- /.post-head -->
    <div class="img-container">
      <v-img
        :src="post.userProfile.img"
        contain
        max-height="597"
        min-height="479"
      ></v-img>
    </div>
    <!-- /.img-container -->
    <post-icon></post-icon>
    <like :like="post.like" />
    <post-text
      :userName="post.userProfile.name"
      :text="post.content.text"
    ></post-text>
    <comment
      :comments="post.comments"
      :user-img="post.userProfile.img"
      :index="index"
    />
  </div>
</template>

<script>
export default {
  name: 'Post',
  props: ['post', 'index'],
  components: {
    PostIcon: () => import('@/components/main/PostIcon.vue'),
    Like: () => import('@/components/main/Like.vue'),
    PostText: () => import('@/components/main/PostText.vue'),
    Comment: () => import('@/components/main/Comment.vue'),
  },
};
</script>

<style lang="scss" scoped>
.post-head {
  height: 60px;
  width: 100%;
  border-bottom: 1px solid #80808054;
  .head-avatar {
    margin-left: 20px;
  }
  h3 {
    font-weight: bold;
    display: inline-block;
    margin: 0 20px;
  }
}
</style>
