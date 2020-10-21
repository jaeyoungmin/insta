<template>
  <div>
    <v-card>
      <v-row class="card-title" justify="center" align="center">
        <v-btn icon @click="dialog = false"><v-icon>mdi-close</v-icon></v-btn>
        <v-spacer></v-spacer>
        <h3>댓글</h3>
        <v-spacer></v-spacer>
        <v-btn icon><v-icon>mdi-send</v-icon></v-btn>
      </v-row>
      <!-- /.card-title -->
      <v-row no-gutters align="center" class="comment-text-field-wrapper">
        <v-avatar><v-img :src="userImg"></v-img></v-avatar>
        <v-text-field
          solo
          flat
          rounded
          placeholder="댓글 달기..."
          class="add-comment-text-field"
          v-model="myComment"
        >
          <template v-slot:append>
            <v-btn text large color="blue" @click="pushComment">게시</v-btn>
          </template>
        </v-text-field>
      </v-row>
      <div class="like-user-list">
        <v-row
          v-for="(comment, i) in comments"
          :key="i"
          class="list-item"
          no-gutters
          align="start"
        >
          <p>
            <strong>{{ comment.name }}</strong> {{ comment.text }}
          </p>
          <v-spcaer></v-spcaer>
          <v-btn icon x-small><v-icon>mdi-heart-outline</v-icon></v-btn>
        </v-row>
      </div>
      <!-- /.like-user-list -->
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'CommentPush',
  props: ['comments', 'userImg', 'index'],
  data() {
    return {
      myComment: '',
    };
  },
  methods: {
    pushComment() {
      this.$store.commit('pushComment', {
        index: this.index,
        name: 'me',
        text: this.myComment,
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.like-container {
  padding: 0 16px;
}
.card-title {
  height: 60px;
  padding: 0 20px;
  border: 1px solid #80808054;
  h3 {
    display: inline-block;
  }
}
.comment-text-field-wrapper {
  padding: 10px 15px;
  background-color: #eee;
}
.add-comment-text-field {
  height: 50px;
  margin-left: 10px;
}
.list-item {
  padding: 16px;
  p {
    margin: 0;
    max-width: 90%;
  }
}
</style>
