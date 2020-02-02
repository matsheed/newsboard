<template>
  <v-app>
    <!-- Navigation -->
    <navigation-drawer></navigation-drawer>

    <v-content>
      <news-board />
    </v-content>
  </v-app>
</template>

<script>
import NewsBoard from "./components/NewsBoard";
import NavigationDrawer from "./components/NavigationDrawer";

export default {
  name: "App",

  components: {
    NewsBoard,
    NavigationDrawer
  },

  data: () => ({
    //
  })
};
</script>

