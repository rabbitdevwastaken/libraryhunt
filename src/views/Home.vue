<template>
  <v-container>
    <v-row>
      <v-col>
        <search-filed />
      </v-col>
    </v-row>
    <post-list />
  </v-container>
</template>

<script>
import PostList from '../components/main/posts/PostList.vue';
import SearchFiled from '../components/main/SearchFiled.vue';

export default {
  components: { PostList, SearchFiled },
  name: 'Home',
};
</script>
