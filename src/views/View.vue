<template>
  <v-container>
    <v-row>
      <v-col>
        <v-btn color="white" small depressed fab>
          <v-icon>mdi-arrow-left</v-icon>
        </v-btn>
      </v-col>
      <v-spacer></v-spacer>
      <v-col>
        <v-btn block depressed color="primary">12 | Upvote</v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card rounded="lg" flat color="pa-4">
          <v-card-title>Project Name</v-card-title>
          <v-card-actions>
            <v-btn text small v-for="tag in 3" :key="tag">#tag-{{ tag }}</v-btn>
          </v-card-actions>
          <v-card-text>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iure, nostrum quae. Ipsum,
            magni aspernatur cumque architecto similique odit est quaerat quidem nostrum molestias
            vel explicabo temporibus omnis dignissimos corporis voluptas.
          </v-card-text>
          <v-card-actions>
            <profile-card />
            <v-spacer></v-spacer>
            <v-btn depressed color="primary">Comment</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <div class="caption px-4">
          Created at: 12/12/12
        </div>
        <div class="caption px-4">
          2 Comments
        </div>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" v-for="comment in 3" :key="comment">
        <comment-card />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import CommentCard from '../components/main/comments/CommentCard.vue';
import ProfileCard from '../components/main/profile/ProfileCard.vue';

export default {
  components: { CommentCard, ProfileCard },
  name: 'Home',
};
</script>
