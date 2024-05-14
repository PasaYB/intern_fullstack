<template>
  <v-app>
    <appheader :color="color" :flat="flat" />
    <v-main class="pt-0">
      <appprofile />
      <appproject />
      <appgit />
      <appplans />
      <appcontact />
    </v-main>
    <v-scale-transition>
      <v-btn
        fab
        v-show="fab"
        v-scroll="onScroll"
        dark
        fixed
        bottom
        right
        color="secondary"
        @click="toTop"
      >
        <v-icon>mdi-arrow-up</v-icon>
      </v-btn>
    </v-scale-transition>
    <appfooter />
  </v-app>
</template>

<style scoped>
.v-main {
  background-color: white;
  background-attachment: fixed;
  background-position: center;
  background-size: cover;
}
</style>

<script>
import appheader from "./components/appheader";
import appfooter from "./components/appfooter";
import appprofile from "./components/appprofile";
import appproject from "./components/appproject";
import appgit from "./components/appgit";
import appplans from "./components/appplans";
import appcontact from "./components/appcontact";

export default {
  name: "App",

  components: {
    appheader,
    appfooter,
    appprofile,
    appproject,
    appgit,
    appplans,
    appcontact,
  },

  data: () => ({
    fab: null,
    color: "",
    flat: null,
  }),

  created() {
    const top = window.pageYOffset || 0;
    if (top <= 60) {
      this.color = "transparent";
      this.flat = true;
    }
  },

  watch: {
    fab(value) {
      if (value) {
        this.color = "secondary";
        this.flat = false;
      } else {
        this.color = "transparent";
        this.flat = true;
      }
    },
  },

  methods: {
    onScroll(e) {
      if (typeof window === "undefined") return;
      const top = window.pageYOffset || e.target.scrollTop || 0;
      this.fab = top > 60;
    },
    toTop() {
      this.$vuetify.goTo(0);
    },
  },
};
</script>
