<template>
  <v-bottom-navigation fixed background-color="headings" color="white">
    <v-btn icon style="margin: 2px;" href="https://github.com/milindvishnoi">
      <v-icon x-large>mdi-github</v-icon>
    </v-btn>
    <v-btn icon style="margin: 2px;" href="https://www.linkedin.com/in/milindvishnoi/">
      <v-icon x-large>mdi-linkedin</v-icon>
    </v-btn>
    <v-btn icon style="margin: 2px;" href="/Milind_Vishnoi_CV.pdf" download>
      <v-icon large>mdi-file-download</v-icon>
    </v-btn>
    <!-- Disabled Light Mode -->
    <v-btn
      v-if="$vuetify.theme.dark"
      @click="$vuetify.theme.dark = ! $vuetify.theme.dark"
      icon
      color="nav"
    >
      <v-icon x-large>mdi-weather-sunny</v-icon>
    </v-btn>
    <v-btn v-else @click="$vuetify.theme.dark = ! $vuetify.theme.dark" icon color="nav">
      <v-icon x-large>mdi-weather-night</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>