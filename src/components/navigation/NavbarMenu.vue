<template>
  <div>

    <v-app-bar
      color="green darken-3"
      dark
      fixed app clipped-left dense
    >
      <v-app-bar-nav-icon @click="toggleSidebar()"></v-app-bar-nav-icon>


      <v-spacer>
        <v-toolbar-title>[NAME]</v-toolbar-title>
      </v-spacer>

      <v-btn icon>
        <v-icon>mdi-logout</v-icon>
      </v-btn>
      
    </v-app-bar>

    <v-navigation-drawer
      v-model="sidebar"
      clipped
      app
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-green--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Sauvegardes</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Administration</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Documentation</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
/* eslint-disable */
  export default {
    data: () => ({
      drawer: false,
      group: null,
      sidebar: false,
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
    mounted() {
      //
    },  
    methods: {
      toggleSidebar() {
        this.sidebar = !this.sidebar
      },
    }
  }

</script>

<style>
</style>