<template>
  <v-text-field
    v-model="search"
    solo
    flat
    hide-details
    append-icon="mdi-magnify"
    label="Search Libraries"
    single-line
  ></v-text-field>
</template>

<script>
export default {
  data() {
    return {
      search: '',
    };
  },
};
</script>

<style></style>
