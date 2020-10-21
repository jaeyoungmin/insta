<template>
  <div class="comment-container">
    <div class="button-wrapper">
      <v-dialog v-model="dialog" width="500">
        <template v-slot:activator="{ on, attrs }">
          <button v-bind="attrs" v-on="on">
            댓글 {{ comments.length }}개 모두보기
          </button>
          <!-- /.button-wrapper -->
        </template>
        <!-- comentpush 연결 -->
        <comment-push
          :comments="comments"
          :user-img="userImg"
          :index="index"
        ></comment-push>
      </v-dialog>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Comment',
  props: ['comments', 'userImg', 'index'],
  components: {
    CommentPush: () => import('@/components/main/CommentPush.vue'),
  },
  data() {
    return {
      dialog: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.comment-container {
  padding: 0 16px;
}
.comments-wrapper {
  padding: 10px;
  p {
    margin-bottom: 0;
  }
}
.button-wrapper {
  button {
    color: gray;
    margin-bottom: 5px;
  }
}
</style>
