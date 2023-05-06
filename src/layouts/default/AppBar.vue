<script   setup>
//
import {ref,onMounted} from "vue";

const menuItems = ['menu1','menu2'];

</script>

<template>

    <v-app-bar color="primary" flat>
      <v-container class="fill-height d-flex align-center">
        <v-toolbar-title>Application Name</v-toolbar-title>

        <v-btn
          v-for="link in menuItems"
          :key="link"
          variant="text"
        >
          {{ link }}
        </v-btn>

        <v-spacer></v-spacer>

        <v-responsive max-width="260">
          <v-text-field
            density="compact"
            hide-details
            variant="solo"
          ></v-text-field>
        </v-responsive>
      </v-container>
    </v-app-bar>
</template>

