<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer">
      <v-list
          :lines="false"
          nav
        >
        <v-list-subheader>Menu principale</v-list-subheader>

          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :value="item"
            active-color="primary"
            :prepend-icon="item.icon"
          >
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item>
        </v-list>
    </v-navigation-drawer>

    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-app-bar-title>Application</v-app-bar-title>

      <v-app-bar-actions>
        <v-btn icon>
          <v-icon>mdi-account</v-icon>
        </v-btn>
      </v-app-bar-actions>
    </v-app-bar>

    <v-main>
      <!--  -->
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    drawer:true,
    items: [
        { text: 'Acceuil', icon: 'mdi-home' },
        { text: 'Page 2', icon: 'mdi-folder' }
      ],
  }),
}
</script>
