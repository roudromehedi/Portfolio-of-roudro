<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Web</span>
      <span class="green--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="project.dialog"
        lazy
        max-width="1000"
        v-for="project in projects"
        :key="project.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="230"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              ></v-img>
              <v-card-title primary-title class="justify-center">{{
                project.title
              }}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-img :src="project.poster"></v-img>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="green" text-color="white">{{
              project.tech.tech1
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech2
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech3
            }}</v-chip>
            <v-chip color="green" text-color="white">{{
              project.tech.tech4
            }}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn
              flat
              large
              dark
              color="green"
              :href="project.git"
              target="_blank"
            >
              <v-icon left>fab fa-github</v-icon>GitHub
            </v-btn>
            <v-btn
              large
              flat
              dark
              color="green"
              :href="project.demo"
              target="_blank"
            >
              <v-icon left>fas fa-desktop</v-icon>Demo
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: "Web Portfolio",
    titleTemplate: "%s ← Roudro",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Eldin Zaimovic's Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Eldin' Space" },
      { property: "og:site_name", content: "Eldin' Space" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://eldin.space" },
      {
        property: "og:image",
        content: ""
      },
      {
        property: "og:description",
        content:
          "Eldin Zaimovic's Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
      }
    ]
  },
  data() {
    return {
      dialog: false,
      projects: [
        {
          dialog: false,
          title: "Movie Ticket Booking System With Admin Dashboard",
          git: "https://github.com/roudromehedi/cineplex",
          demo: "https://cineplex.smroudro.com/",
          tech: {
            tech1: "Vue 3",
            tech2: "JavaScript",
            tech3: "Bootstrap 5",
            tech4: "Vuetify",
            tech4: "Json Server"
          },
          poster: "https://i.imgur.com/f9LgAJ5.png"
        },
        {
          dialog: false,
          title: "Quiz App",
          git: "https://github.com/roudromehedi/Vue-Quiz-App",
          demo: "https://quiz.smroudro.com/",
          tech: {
            tech1: "Vue 3",
            tech2: "JavaScript",
            tech3: "Tailwind CSS",
            tech4: "SCSS"
          },
          poster: "https://i.imgur.com/VuD3e5N.png"
        },
        {
          dialog: false,
          title: "Expense Tracker Pro",
          git: "https://github.com/roudromehedi/ExpenseTrackerPro",
          demo: "https://expensetrackerpro.smroudro.com/",
          tech: {
            tech1: "Vue",
            tech2: "JavaScript",
            tech3: "Node JS",
            tech4: "Express",
            tech5: "Mongo DB",
            tech6: "Vuetify",
            tech7: "SCSS"
          },
          poster: "https://i.imgur.com/9qe9qRx.png"
        },
        {
          dialog: false,
          title: "WeatherCast",
          git: "https://github.com/roudromehedi/weather-cast",
          demo: "https://weathercast.smroudro.com/",
          tech: {
            tech1: "Vue",
            tech2: "JavaScript",
            tech3: "TypeScript",
            tech4: "Vuetify",
            tech5: "SCSS"
          },
          poster: "https://i.imgur.com/1GueHpk.png"
        },
        {
          dialog: false,
          title: "E-Commerce",
          git:
            "https://github.com/roudromehedi/E-commerce-site-with-vue-js-vuetify",
          demo: "https://ecom.smroudro.com/",
          tech: {
            tech1: "VUE",
            tech2: "Vuetify",
            tech3: "HTML",
            tech4: "JavaScript"
          },
          poster: "https://i.imgur.com/0KY2ufA.png"
        },
        {
          dialog: false,
          title: "Github Profile search",
          git: "https://github.com/roudromehedi/Github-Profile-fetcher",
          demo: "https://gitpro.smroudro.com/",
          tech: {
            tech1: "JavaScript",
            tech2: "SCSS",
            tech3: "HTML"
          },
          poster: "https://i.imgur.com/QX8BI8m.png"
        }
      ]
    };
  }
};
</script>

<style scoped></style>
