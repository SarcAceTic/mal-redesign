<script setup>
const someList = [
  { name: 'Anime', options: ['Top', 'Seasonal', 'Recommendations', 'Reviews', 'Videos'] },
  { name: 'Manga', options: ['Top', 'Store', 'Reviews', 'Recommendations'] },
  { name: 'Community', options: ['Interest Stacks', 'Forums', 'Clubs', 'Users', 'Blogs'] },
  { name: 'Industry', options: ['News', 'Articles', 'People', 'Characters', 'Companies']},
  { name: 'Watch', options: ['Episode Videos', 'Trailers']},
  { name: 'Help', options: ['About', 'Support', 'Advertising', 'FAQ', 'Report', 'Staff']}
]
</script>

<template>
  <header class="w-100 text-center">
    <section class="bg-grey-darken-4 background-image">
      <v-container>
        <v-row class="align-center" no-gutters>
          <v-col cols="2" class="text-left">
            <h1>MyAnimeList</h1>
          </v-col>
          <v-divider vertical></v-divider>
          <v-col><h3>Anime List</h3> </v-col>
          <v-col><h3>Manga List</h3> </v-col>
          <v-col><h3>Quick Add</h3> </v-col>
          <v-divider vertical></v-divider>
          <v-col>
            <v-icon size="30">mdi-email</v-icon>
          </v-col>
          <v-divider vertical></v-divider>
          <v-col>
            <v-icon size="30">mdi-bell</v-icon>
          </v-col>
          <v-divider vertical></v-divider>
          <v-col class="">
            <h4>SarcAceTic</h4>
          </v-col>
          <v-col>
            <v-avatar size="40">
              <v-img src="/MyPFP.jpg"></v-img>
            </v-avatar>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="mt-2">
      <v-container>
        <v-row class="align-center text-left" no-gutters>
          <v-col class="ma-3" v-for="item in someList">
            <v-btn block variant="outlined" class="pa-6 stfu" color="blue">
              <h3>{{ item.name }}</h3>
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </header>
</template>

<style scoped>
.background-image {
  background-image: url('../assets/backkkground.jpg');
}
</style>
