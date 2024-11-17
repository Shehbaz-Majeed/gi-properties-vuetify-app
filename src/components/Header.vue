<template>
  <v-app-bar
    color="primary"
    prominent
  >
    <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

    <v-toolbar-title>My files</v-toolbar-title>

    <v-spacer></v-spacer>

    <template v-if="$vuetify.display.mdAndUp">
      <v-btn icon="mdi-magnify" variant="text"></v-btn>

      <v-btn icon="mdi-filter" variant="text"></v-btn>
    </template>

    <v-btn icon="mdi-dots-vertical" variant="text"></v-btn>
  </v-app-bar>

  <v-navigation-drawer
    v-model="drawer"
    :location="$vuetify.display.mobile ? 'left' : undefined"
    temporary
  >
    <v-list
      :items="items"
    ></v-list>
  </v-navigation-drawer>
</template>

<script>

  export default {
    data: () => ({
      drawer: false,
      group: null,
      items: [
        {
          title: 'Buy',
          value: 'buy',
        },
        {
          title: 'Rent',
          value: 'rent',
        },
        {
          title: 'Projects',
          value: 'projects',
        },
        {
          title: 'Developer',
          value: 'developer',
        },
        {
          title: 'Areas',
          value: 'areas',
        },
        {
          title: 'Services',
          value: 'services',
        },
        {
          title: 'blogs',
          value: 'blogs',
        },
        {
          title: 'More',
          value: 'more',
        },
      ],
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>