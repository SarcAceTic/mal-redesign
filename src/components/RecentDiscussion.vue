<script setup>
const discussionList = [
  {
    username: 'SarcAceTic',
    question:
      'What initially drew you to the world of anime, and do you remember the first anime that left a lasting impression on you?',
    imageUrl: '/MyPFP.jpg',
    heart: 400,
    replies: 100
  },
  {
    username: 'JUNko',
    question:
      'If you could live in the universe of any anime, which one would it be and why? What role would you want to play in that world?',
    imageUrl: '/pfp3.jpeg',
    heart: 39,
    replies: 26
  },
  {
    username: 'theNEGATIVEfurther',
    question:
      'Anime often explores deep themes and emotions. Can you share a moment from any anime that had a profound impact on you or made you reflect on life?',
    imageUrl: '/pfp2.jpeg',
    heart: 83,
    replies: 35
  },
  {
    username: 'extremeconditions',
    question:
      "In the realm of anime, there are various genres. What's a genre you initially hesitated to explore but ended up loving? Any recommendations?",
    imageUrl: '/pfp4.jpg',
    heart: 76,
    replies: 44
  },
  {
    username: 'Payload',
    question:
      'Anime characters often undergo significant development. Is there a character arc that resonated with you personally, and why?',
    imageUrl: '/pfp5.jpg',
    heart: 40,
    replies: 68
  },
  {
    username: 'your_girlfriend',
    question:
      'If you could bring one anime character to life and have a conversation with them, who would it be and what would you ask them?',
    imageUrl: '/pfp6.jpg',
    heart: 53,
    replies: 48
  }
]
const topAnime = {
  name: 'Oshi No Ko',
  description:
    "Opening his eyes in the lap of his beloved idol, Gorou finds that he has been reborn as Aquamarine Hoshino—Ai's newborn son! With his world turned upside down, Gorou soon learns that the world of showbiz is paved with thorns, where talent does not always beget success. Will he manage to protect Ai's smile that he loves so much with the help of an eccentric and unexpected ally?",
  imageUrl: [
    'https://m.media-amazon.com/images/M/MV5BYTgxZjNlZWQtYjg1OS00NzY2LTkyZTctZDBkY2Y2ZWEyMjNlXkEyXkFqcGdeQXVyMzgxODM4NjM@._V1_.jpg',
    'https://cdn0-production-images-kly.akamaized.net/gcliNvvkt5VcJAAGnicqJwBhGKo=/800x1066/smart/filters:quality(75):strip_icc():format(webp)/kly-media-production/medias/4393532/original/035045700_1681367582-MV5BZWRhNWQ2NGUtOTdkYy00ZDBmLWFjMTktNTE4NzY0OGYzZGQ3XkEyXkFqcGdeQXVyMzgxODM4NjM_._V1_.jpg',
    'https://i.redd.it/6ahm7k9gva5a1.jpg'
  ],
  rating: 5
}
const topManga = {
  name: ''
}
</script>

<template>
  <section>
    <v-container>
      <v-row>
        <v-col cols="11" lg="6"
          ><h2 class="my-4 mb-8">Recent Discussions</h2>
          <v-list class="bg-transparent" lines="three">
            <v-row v-for="disc in discussionList" no-gutters class="justify-start">
              <v-col cols="12">
                <v-list-item :prepend-avatar="disc.imageUrl">
                  <v-list-item-title
                    ><h3>{{ disc.username }}</h3></v-list-item-title
                  >
                  <v-list-item-subtitle class="my-2 mb-4"
                    ><p>{{ disc.question }}</p></v-list-item-subtitle
                  >
                  <v-list-action>
                    <v-row no-gutters class="justify-start">
                      <v-col cols="3" md="3">
                        <v-icon size="28" class="mr-1">mdi-heart-outline</v-icon>
                        <span>{{ disc.heart }}</span>
                      </v-col>
                      <v-col cols="3" md="3">
                        <v-icon size="28" class="mr-1">mdi-forum-outline</v-icon>
                        <span>{{ disc.replies }}</span>
                      </v-col>
                      <v-col cols="3" md="3">
                        <v-icon size="28">mdi-share-outline</v-icon>
                      </v-col>
                    </v-row>
                  </v-list-action>
                </v-list-item>
                <v-divider inset></v-divider>
              </v-col>
            </v-row> </v-list
        ></v-col>
        <v-col cols="12" sm="12" lg="6">
          <h2 class="my-4 mb-8">Top Anime 2023</h2>
          <v-row
            ><v-col class="d-flex flex-column flex-sm-column flex-md-row flex-lg-row">
              <v-carousel class="listing-div flex-lg-1-0"
                  hide-delimiters
                  cycle
                  :show-arrows="false"
                >
                <v-carousel-item
                  v-for="img in topAnime.imageUrl"
                  cover
                  :src="img"
                ></v-carousel-item
              ></v-carousel>
              <div class="" >
                <h3 class="mb-2 mt-n2">Oshi No Ko</h3>
                <p class="text-left">{{ topAnime.description }}</p>
                <v-rating
                  active-color="blue"
                  color="blue"
                  readonly
                  half-increments
                  v-model="topAnime.rating"
                ></v-rating>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

h1,
h2,
h3,
h4,
h5,
h6,
p,
span {
  font-family: 'Poppins', sans-serif;
}
h1 {
  font-weight: 800 !important;
}

h2 {
  font-weight: 700 !important;
}

h3 {
  font-weight: 600 !important;
}
h4,
span {
  font-weight: 500 !important;
}
p {
  font-weight: 400 !important;
}
</style>
