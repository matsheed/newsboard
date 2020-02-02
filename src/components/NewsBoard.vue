<template>
  <v-card>
    <v-container>
      <!-- Create column -->
      <v-row dense>
        <!-- card-column  -->
        <v-col :cols="col.flex" v-for="(col, i) in cols" :key="i">
          <!-- Card -->
          <v-card class="my-2" dark v-for="(card, i) in cards" :key="i">
            <v-card-title class="headline">{{ card.title }}</v-card-title>
            <v-card-subtitle>{{ card.subtitle }}</v-card-subtitle>
            <v-card-text>{{ card.text }}</v-card-text>
            <v-card-actions>
              <v-btn :href="card.href">Klicka inte här</v-btn>
            </v-card-actions>
            <v-spacer></v-spacer>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  name: "NewBoard",

  data: () => ({
    cards: [
      {
        id: 1,
        title: "Allt flyter på med den nya...",
        subtitle: "",
        text: "This is a long text, This is a long text, This is a long text",
        href: "https://github.com/vuetifyjs/vuetify-loader"
      },
      {
        id: 2,
        title: "vuetify-loader",
        subtitle: "",
        text: "This is a long text",
        href: "https://github.com/vuetifyjs/vuetify-loader"
      },
      {
        id: 3,
        title: "vuetify-loader",
        subtitle: "",
        text: "This is a long text",
        href: "https://github.com/vuetifyjs/vuetify-loader"
      }
    ],
    cols: [
      {
        id: 1,
        name: "One",
        flex: 4
      },
      {
        id: 2,
        name: "Two",
        flex: 4
      },
      {
        id: 3,
        name: "Three",
        flex: 4
      }
    ]
  })
};
</script>
