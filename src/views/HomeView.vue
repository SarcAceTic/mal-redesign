<script setup>
import MainHeader from '../components/MainHeader.vue'
import LatestAnime from '../components/LatestAnime.vue'
import LatestManga from '../components/LatestManga.vue'
import RecentDiscussion from '../components/RecentDiscussion.vue';
</script>

<template>
  <MainHeader />
  <v-divider></v-divider>
  <main class="mt-5">
    <LatestAnime />
    <v-divider></v-divider>
    <LatestManga />
    <v-divider></v-divider>
    <RecentDiscussion />
  </main>
</template>

<style scoped>

</style>
