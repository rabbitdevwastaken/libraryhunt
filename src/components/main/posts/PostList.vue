<template>
  <v-row>
    <v-col class="py-1" v-for="post in 15" :key="post">
      <post-card></post-card>
    </v-col>
  </v-row>
</template>

<script>
import PostCard from './PostCard.vue';

export default {
  components: { PostCard },
};
</script>

<style></style>
