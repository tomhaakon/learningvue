<template>
  <v-app>
    <Navbar></Navbar>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import Navbar from "@/components/global/navbar.vue";
export default {
  name: "App",
  components: {
    Navbar,
  },

  data: () => ({
    //
  }),
};
</script>
