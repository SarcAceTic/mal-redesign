<script setup>
const animeList = [
  {
    title: 'Attack on Titan',
    description:
      'In a world where humanity resides within enormous walled cities to protect themselves from Titans, gigantic humanoid creatures, the story follows Eren Yeager and his friends who join the military to fight the Titans.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BNDFjYTIxMjctYTQ2ZC00OGQ4LWE3OGYtNDdiMzNiNDZlMDAwXkEyXkFqcGdeQXVyNzI3NjY3NjQ@._V1_FMjpg_UX1000_.jpg',
    rating: 4.7
  },
  {
    title: 'My Hero Academia',
    description:
      'Izuku Midoriya, a quirkless boy, enrolls in a prestigious hero academy to pursue his dream of becoming the greatest hero, despite facing challenges and powerful villains.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BOGZmYjdjN2UtNjAwZi00YmEyLWFhNTEtNjM1OTc5ODg0MGEyXkEyXkFqcGdeQXVyMTA1NjQyNjkw._V1_FMjpg_UX1000_.jpg',
    rating: 4.5
  },
  {
    title: 'One Piece',
    description:
      'Monkey D. Luffy sets out on a journey to find the legendary One Piece and become the Pirate King, gathering a diverse crew of talented individuals along the way.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BODcwNWE3OTMtMDc3MS00NDFjLWE1OTAtNDU3NjgxODMxY2UyXkEyXkFqcGdeQXVyNTAyODkwOQ@@._V1_FMjpg_UX1000_.jpg',
    rating: 4.3
  },
  {
    title: 'Demon Slayer',
    description:
      'Tanjiro Kamado becomes a demon slayer to avenge his family and save his demon-turned sister, Nezuko, while battling powerful demons and uncovering the mysteries of his world.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BZjZjNzI5MDctY2Y4YS00NmM4LTljMmItZTFkOTExNGI3ODRhXkEyXkFqcGdeQXVyNjc3MjQzNTI@._V1_.jpg',
    rating: 4.4
  },
  {
    title: 'Naruto',
    description:
      'Naruto Uzumaki, a young ninja with dreams of becoming the strongest ninja and earning the title of Hokage, faces challenges and adversaries as he grows and matures.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BZmQ5NGFiNWEtMmMyMC00MDdiLTg4YjktOGY5Yzc2MDUxMTE1XkEyXkFqcGdeQXVyNTA4NzY1MzY@._V1_FMjpg_UX1000_.jpg',
    rating: 4.9
  },
  {
    title: 'Death Note',
    description:
      'Light Yagami gains possession of a Death Note, a notebook with the power to kill anyone whose name is written in it. He decides to use it to eliminate criminals and become the god of a new world.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BNjRiNmNjMmMtN2U2Yi00ODgxLTk3OTMtMmI1MTI1NjYyZTEzXkEyXkFqcGdeQXVyNjAwNDUxODI@._V1_FMjpg_UX1000_.jpg',
    rating: 4.7
  },
  {
    title: 'Fullmetal Alchemist: Brotherhood',
    description:
      "Brothers Edward and Alphonse Elric use alchemy in their quest to find the Philosopher's Stone and restore their bodies after a failed alchemical experiment.",
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BZmEzN2YzOTItMDI5MS00MGU4LWI1NWQtOTg5ZThhNGQwYTEzXkEyXkFqcGdeQXVyNTA4NzY1MzY@._V1_FMjpg_UX1000_.jpg',
    rating: 4.4
  },
  {
    title: 'Hunter x Hunter',
    description:
      'Gon Freecss aspires to become a Hunter and find his missing father. Along the way, he makes friends, faces formidable foes, and uncovers the secrets of the Hunter world.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BNGM0YTk3MWEtN2JlZC00ZmZmLWIwMDktZTMxZGE5Zjc2MGExXkEyXkFqcGdeQXVyNjAwNDUxODI@._V1_FMjpg_UX1000_.jpg',
    rating: 4.4
  },
  {
    title: 'Sword Art Online',
    description:
      "Players find themselves trapped in a virtual reality MMORPG, where death in the game means death in real life. Kirito must navigate the game's challenges to survive and escape.",
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BYjY4MDU2YjMtNzY1MC00ODg1LWIwMzYtMWE5YTA3YTI4ZjMxXkEyXkFqcGdeQXVyMTMxODk2OTU@._V1_FMjpg_UX1000_.jpg',
    rating: 4.7
  },
  {
    title: 'Cowboy Bebop',
    description:
      'Spike Spiegel and his bounty hunter crew travel through space in the spaceship Bebop, chasing criminals and dealing with their own troubled pasts.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BZDEzMjlkNDgtZjhkNi00N2RlLWFhZTYtNDE5OTc2NjZkODJlXkEyXkFqcGdeQXVyNjAwNDUxODI@._V1_.jpg',
    rating: 4.6
  }
]
</script>

<template>
  <section class="mb-8">
    <v-container>
      <h2 class="my-4 mb-8">Latest Anime</h2>
      <v-row no-gutters>
        <v-col>
          <v-slide-group show-arrows>
            <v-slide-group-item v-for="anime in animeList">
              <div class="listing-div pa-4 mx-4">
                <v-tooltip class="text-center" width="400px" location="end" activator="parent">
                  <p class="text-left">
                    {{ anime.description }}
                  </p>
                  <v-rating
                    active-color="blue"
                    color="blue"
                    readonly
                    half-increments
                    v-model="anime.rating"
                  ></v-rating>
                  <pre class="text-center">{{ anime.rating }}</pre>
                </v-tooltip>
                <div class="overlaaaayy"></div>
                <div
                  class="listing-image"
                  :style="{ backgroundImage: 'url(' + anime.imageUrl + ')' }"
                ></div>
                <h3>{{ anime.title }}</h3>
              </div>
            </v-slide-group-item>
          </v-slide-group>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

p {
  font-family: 'Poppins', sans-serif !important;
}
</style>
