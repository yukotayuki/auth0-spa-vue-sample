<script setup>
import NavigationBar from './components/NavigationBar.vue'
import Auth0User from './components/Auth0User.vue';
</script>

<template>
  <v-app>
    <navigation-bar></navigation-bar>
    <v-main>
      <auth0-user></auth0-user>
    </v-main>
  </v-app>
</template>
