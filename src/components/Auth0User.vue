<script setup>
import { useAuth0 } from '@auth0/auth0-vue'

const { isAuthenticated, user }  = useAuth0()
</script>

<template>
    <div class="mt-4"></div>
    <v-card title="User Profile" color="#86c6da" theme="dark">
        <v-card-text v-if="isAuthenticated">
            <v-code>
                {{ user }}
            </v-code>
        </v-card-text>
        <v-card-text v-else>
            User infomation will be displayed after login
        </v-card-text>
    </v-card>

</template>
