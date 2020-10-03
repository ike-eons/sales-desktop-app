<template>
  <v-app style="-webkit-app-region: drag">

    <Navigation />

    <v-content class="background-color">
      <v-container
        class="scroll-y"
        fluid
      >
        <router-view  :key="$route.path" />
      </v-container>
        <v-btn
          v-scroll="onScroll"
          bottom
          color="red"
          dark
          fab
          fixed
          right
          @click="toTop"
          class="clickable"
        >
          <v-icon>mdi-chevron-up</v-icon>
        </v-btn>
    </v-content><v-content class="background-color">
      <v-container
        class="scroll-y"
        fluid
      >
        <router-view  :key="$route.path" />
      </v-container>
        <v-btn
          v-scroll="onScroll"
          bottom
          color="red"
          dark
          fab
          fixed
          right
          @click="toTop"
          class="clickable"
        >
          <v-icon>mdi-chevron-up</v-icon>
        </v-btn>
    </v-content>

    
  </v-app>
</template>

<script>

import Navigation from './views/components/Navigation'
export default {
  name: 'App',

  components: {
   Navigation,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
  .background-color{
    background-color: #ededed;
  }
</style>
