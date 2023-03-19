<template>
  <v-layout column justify-center align-center class="mt-4 pt-2">
    <img src="https://i.imgur.com/PEVIvXW.png" />

    <br />

    <vue-typer
      class="headline"
      :repeat="0"
      text="S M Roudro Mehedi"
    ></vue-typer>
    <vue-typer
      :text="text1"
      :repeat="Infinity"
      :shuffle="false"
      initial-action="erasing"
      :pre-type-delay="70"
      :type-delay="70"
      :pre-erase-delay="1980"
      :erase-delay="150"
      erase-style="select-back"
      :erase-on-complete="false"
      caret-animation="smooth"
    ></vue-typer>
    <br />
    <v-flex xs12 sm6 md4 lg4 xl4>
      <v-card flat color="transparent" max-width="500">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">
              <span>About</span>
              <span class="green--text">Me</span>
            </h3>
            <div class="d-flex text-center">
              <p class="flex-grow-1">
                Welcome to my portfolio website! My name is Roudro and I'm a
                Front-End Developer based in Germany. I have a passion for
                designing and developing innovative and engaging websites that
                bring ideas to life on the internet. With expertise in various
                front-end technologies, I aim to create intuitive and
                user-friendly interfaces that deliver seamless user experiences.
                Whether you need a simple landing page or a complex web
                application, I'm here to turn your vision into reality. Browse
                my portfolio to see some of my latest projects and let's work
                together to build something amazing.
              </p>
            </div>
          </div>
        </v-card-title>

        <v-card-actions class="hidden-sm-and-down justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            small
            fab
            dark
            outline
            color="green"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from "vue-typer";
import VueCompareImage from "vue-compare-image";

export default {
  metaInfo: {
    title: "Home",
    titleTemplate: "%s ← Roudro",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      { name: "description", content: "Eldin Zaimovic's Portfolio" },
      { charset: "utf-8" },
      { property: "og:title", content: "Eldin' Space" },
      { property: "og:site_name", content: "Eldin' Space" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://eldin.space" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg"
      },
      { property: "og:description", content: "Eldin Zaimovic's Portfolio" }
    ]
  },
  components: {
    "vue-typer": VueTyper,
    VueCompareImage
  },
  data() {
    return {
      icons: [
        { href: "https://github.com/roudromehedi", icon: "fab fa-github" },

        {
          href: "https://www.linkedin.com/in/roudro",
          icon: "fab fa-linkedin-in"
        },
        {
          href: "https://www.xing.com/profile/SMRoudro_Mehedi/cv",
          icon: "fab fa-xing"
        },
        {
          href: "https://www.facebook.com/s.m.roudro/",
          icon: "fab fa-facebook-f"
        }
      ],
      text1: ["Front-End Developer", "Web Developer", "Web Designer"],
      leftImage: "https://i.imgur.com/PEVIvXW.png",
      rightImage: "https://i.imgur.com/PEVIvXW.png",
      leftImage2: "https://i.imgur.com/SXBitjh.jpg",
      rightImage2: "https://i.imgur.com/Dcz2PGx.jpg",
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5
    };
  }
};
</script>
<style>
@keyframes rocking {
  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}
.vue-typer .custom.char.typed {
  color: green;
}
.vue-typer .custom.char.selected {
  color: #e91e63;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}
.vue-typer .custom.caret.typing {
  background-color: green;
}
.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>
