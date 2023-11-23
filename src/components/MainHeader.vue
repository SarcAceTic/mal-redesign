<script setup>
</script>

<template>
  <header class="w-100 text-center">
    <section class="bg-grey-darken-4 background-image">
      <v-container class="w-100">
        <v-row class="align-center" no-gutters>
          <v-col class="text-left">
            <h3>MyAnimeList</h3>
          </v-col>
          <v-divider vertical></v-divider>
          <v-col>Anime List</v-col>
          <v-col>Manga List</v-col>
          <v-col>Quick Add</v-col>
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
  </header>
</template>

<style scoped>
.background-image {
    background-image: url('../assets/backkkground.jpg');
}
</style>
