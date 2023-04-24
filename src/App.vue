<template>
  <v-app>
    
    <navbar-menu />
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import NavbarMenu from './components/navigation/NavbarMenu.vue';

export default {
  components: { NavbarMenu },
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
