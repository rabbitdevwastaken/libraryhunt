<template>
  <v-card rounded="lg" flat :color="backgroundColor">
    <v-card-actions>
      <profile-card />
      <v-spacer></v-spacer>
      <div class="caption">12/12/12 12:12</div>
    </v-card-actions>

    <v-card-text>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ex nostrum adipisci velit amet
      repellat est in ab quis beatae vel facilis, cumque odit iste eaque quae unde iusto! Debitis,
      asperiores!
    </v-card-text>

    <v-card-actions>
      <v-btn depressed>Like</v-btn>
      <v-spacer></v-spacer>
      <v-btn text>
        <v-icon class="mr-2" color="grey darken-1">mdi-message</v-icon>
        <span>2</span>
      </v-btn>
      <v-btn depressed color="primary">Reply</v-btn>
    </v-card-actions>

    <v-card-text v-if="!hideReplies" class="pl-2">
      <comment-card
        background-color="grey lighten-5"
        v-for="reply in replies"
        :replies="[]"
        :key="reply"
      />
    </v-card-text>
  </v-card>
</template>

<script>
import ProfileCard from '../profile/ProfileCard.vue';

export default {
  name: 'CommentCard',

  props: {
    replies: {
      type: Array,
      default: () => [1, 2, 3],
    },

    backgroundColor: {
      type: String,
      default: '',
    },
  },

  components: { ProfileCard },

  data() {
    return {
      hideReplies: this.replies.length > 5 || this.replies.length === 0,
    };
  },
};
</script>

<style></style>
