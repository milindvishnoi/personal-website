<template>
  <v-app :style="{background: $vuetify.theme.themes[theme].background}">
    <navbar />
    <v-main>
      <!-- Home Page Container -->
      <home-page id="home" />
      <!-- About Me -->
      <v-container class="pt-8" id="aboutme">
        <v-row class="d-flex justify-center">
          <h1
            :class="{'small-h1': this.$vuetify.breakpoint.xs, 'med-h1': this.$vuetify.breakpoint.sm}"
          >Who Am I?</h1>
        </v-row>
        <about-me />
      </v-container>
      <!-- Projects Container -->
      <v-container class="pt-8" id="projects">
        <Projects />
      </v-container>
      <!-- Contact Me Section -->
      <!-- <v-container class="pt-8 align-center" id="contactme">
        <v-row class="d-flex justify-center">
          <h1
            :class="{'small-h1': this.$vuetify.breakpoint.xs, 'med-h1': this.$vuetify.breakpoint.sm}"
          >Get In Touch!</h1>
        </v-row>
        <v-row justify="center">
          <contact-me />
        </v-row>
      </v-container>-->
      <!-- Last Indentation -->
      <div class="footer-space" />
      <footer class="text-center footer-space">Copyright © 2020 Milind Vishnoi</footer>
      <div
        class="footer-space"
      />
    </v-main>
    <bottom-app-bar />
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import BottomAppBar from "./components/BottomAppBar.vue";
import HomePage from "./views/HomePage.vue";
import Projects from "./views/Projects.vue";
import AboutMe from "./views/AboutMe.vue";
// import ContactMe from "./views/ContactMe.vue";

export default {
  name: "App",

  components: {
    HomePage,
    Navbar,
    BottomAppBar,
    Projects,
    AboutMe
    // ContactMe
  },
  computed: {
    theme() {
      return this.$vuetify.theme.dark ? "dark" : "light";
    }
  }
};
</script>

<style>
h1 {
  font-size: 80px;
}
.med-h1 {
  font-size: 60px;
}
.small-h1 {
  font-size: 45px;
}
.website-background {
  background: white;
}
.footer-space {
  height: 50px;
}
</style>