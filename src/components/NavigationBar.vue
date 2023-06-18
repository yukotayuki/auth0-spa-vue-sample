<script setup>
import { useAuth0 } from '@auth0/auth0-vue';

const { isAuthenticated, loginWithRedirect, logout } = useAuth0();

function authLogin() {
  loginWithRedirect();
};
function authLogout() {
  logout({
    logoutParams: {
      returnTo: window.location.origin
    }
  });
};
</script>

<template>
  <v-app-bar>
    <v-app-bar-title>
      Login Demo
    </v-app-bar-title>
    <v-spacer></v-spacer>
    <v-btn v-if="!isAuthenticated" @click="authLogin">Login</v-btn>
    <template v-else>
      <v-btn @click="authLogout">Logout</v-btn>
    </template>
  </v-app-bar>
</template>