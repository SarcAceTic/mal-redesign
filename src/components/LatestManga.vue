<script setup>
const mangaList = [
  {
    title: 'Bleach',
    description:
      'Ichigo Kurosaki accidentally obtains the powers of a Soul Reaper and must protect the living world from evil spirits and guide departed souls to the afterlife.',
    imageUrl: 'https://m.media-amazon.com/images/I/81c18nJYygL._AC_UF1000,1000_QL80_.jpg',
    rating: 4.5
  },
  {
    title: 'Dragon Ball',
    description:
      'Follow the adventures of Goku as he trains in martial arts, explores the world, and defends it from powerful foes, seeking the magical Dragon Balls along the way.',
    imageUrl: 'https://m.media-amazon.com/images/I/81CoMp5wjEL._AC_UF1000,1000_QL80_.jpg',
    rating: 4.7
  },
  {
    title: "JoJo's Bizarre Adventure",
    description:
      'Spanning generations, the Joestar family faces supernatural threats using their unique Stand abilities. Each part introduces new characters and challenges.',
    imageUrl:
      'https://d28hgpri8am2if.cloudfront.net/book_images/onix/cvr9781974724178/jojos-bizarre-adventure-part-5-golden-wind-vol-9-9781974724178_hr.jpg',
    rating: 4.8
  },
  {
    title: 'Nausicaä of the Valley of the Wind',
    description:
      'Set in a post-apocalyptic world, Nausicaä, a princess and environmentalist, navigates political intrigue and battles giant insects to save her people.',
    imageUrl:
      'https://upload.wikimedia.org/wikipedia/en/c/c3/NausicaaCoverTankobon1.png',
    rating: 4.5
  },
  {
    title: 'One Punch Man',
    description:
      'Saitama, a hero who can defeat any opponent with a single punch, seeks meaning and excitement in a world filled with powerful monsters and heroes.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BZjJlNzE5YzEtYzQwYS00NTBjLTk5YzAtYzUwOWQyM2E3OGI2XkEyXkFqcGdeQXVyNTgyNTA4MjM@._V1_.jpg',
    rating: 4.6
  },
  {
    title: 'Blue Exorcist',
    description:
      'Rin Okumura discovers he is the son of Satan. To redeem himself, he enrolls in True Cross Academy to become an exorcist and fight against demonic forces.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BNjYyMjhiNTYtN2M3Yy00NTlhLWJkMmEtMzVhOGEyMzNjNTNhXkEyXkFqcGdeQXVyMzgxODM4NjM@._V1_FMjpg_UX1000_.jpg',
    rating: 4.9
  },
  {
    title: 'The Promised Neverland',
    description:
      'Emma, Norman, and Ray discover the dark truth behind their idyllic orphanage and must escape a sinister fate while facing intelligent and deadly adversaries.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BMTYwYjYyZDgtMTQ3My00YTI4LThmZTUtZmU1MjllOWRlOTdhXkEyXkFqcGdeQXVyMzgxODM4NjM@._V1_FMjpg_UX1000_.jpg',
    rating: 4.4
  },
  {
    title: 'Vinland Saga',
    description:
      'Thorfinn, a young warrior seeking revenge, joins a Viking mercenary group as they explore, trade, and engage in epic battles during the Viking Age.',
    imageUrl:
      'https://upload.wikimedia.org/wikipedia/en/thumb/5/51/Vinland_Saga_volume_01_cover.jpg/220px-Vinland_Saga_volume_01_cover.jpg',
    rating: 4.4
  },
  {
    title: 'Parasyte',
    description:
      'Shinichi Izumi must coexist with a parasitic alien that takes over his right hand. Together, they face other parasitic beings threatening humanity.',
    imageUrl:
      'https://m.media-amazon.com/images/M/MV5BZTViMTZlMjgtNjVmZC00NjEzLWJlN2QtMjQ4ZTYxNzBiZmMyXkEyXkFqcGdeQXVyNjc2NjA5MTU@._V1_FMjpg_UX1000_.jpg',
    rating: 4.7
  },
  {
    title: 'Fruits Basket',
    description:
      'Tohru Honda, after meeting the Sohma family cursed to turn into animals of the Chinese zodiac, becomes involved in their lives and helps break the curse.',
    imageUrl:
      'https://www.crunchyroll.com/imgsrv/display/thumbnail/480x720/catalog/crunchyroll/0a34f193aa46a27cd75f5ee553834c41.jpe',
    rating: 4.8
  }
]
</script>

<template>
  <section class="mb-8">
    <v-container>
      <h2 class="my-4 mb-8">Latest Manga</h2>
      <v-row no-gutters>
        <v-col>
          <v-slide-group show-arrows>
            <v-slide-group-item v-for="manga in mangaList">
              <div class="listing-div pa-4 mx-4">
                <v-tooltip class="text-center" width="400px" location="end" activator="parent">
                  <p class="text-left">
                    {{ manga.description }}
                  </p>
                  <v-rating
                    active-color="blue"
                    color="blue"
                    readonly
                    half-increments
                    v-model="manga.rating"
                  ></v-rating>
                  <pre class="text-center">{{ manga.rating }}</pre>
                </v-tooltip>
                <div class="overlaaaayy"></div>
                <div
                  class="listing-image"
                  :style="{ backgroundImage: 'url(' + manga.imageUrl + ')' }"
                ></div>
                <h3>{{ manga.title }}</h3>
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
