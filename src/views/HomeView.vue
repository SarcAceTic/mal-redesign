<script setup>
import MainHeader from '../components/MainHeader.vue'

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
const mangaList = []
const newsList = []
</script>

<template>
  <MainHeader />
  <main class="mt-5">
    <section>
      <v-container>
        <h2>Latest Anime</h2>
        <v-row class="my-4" no-gutters>
          <v-col class="">
            <v-slide-group class="" show-arrows>
              <v-slide-group-item class="" v-for="anime in animeList">
                <div class="anime-div pa-4 mx-4">
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
                    class="anime-image"
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
  </main>
</template>

<style scoped>
.anime-div {
  position: relative;
  overflow: hidden;
  background-size: 100% 300px;
  width: 200px !important;
  height: 300px !important;
}
.anime-div h3 {
  font-size: 18px;
  letter-spacing: 1px;
  position: relative;
  color: white;
  opacity: 0;
  transition: opacity 0.3s;
}
.anime-image {
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}
.overlaaaayy {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.6);
  opacity: 0;
  transition: opacity 0.3s;
}
.anime-div:hover .overlaaaayy {
  opacity: 1;
}
.anime-div:hover h3 {
  opacity: 1;
}
</style>
