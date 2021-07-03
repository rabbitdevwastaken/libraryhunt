<template>
  <v-app>
    <core-app-bar-mobile />
    <v-main>
      <div class="app-wrapper fill-height">
        <router-view />
      </div>
    </v-main>
  </v-app>
</template>

<script>
import CoreAppBarMobile from './CoreAppBarMobile.vue';

export default {
  components: { CoreAppBarMobile },
};
</script>

<style lang="less" scoped>
.app-wrapper {
  background-color: #f1f1f1;
}
</style>
