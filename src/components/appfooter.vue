<template>
  <v-footer dark padless>
    <v-card tile class="secondary white--text text-center">
      <v-card-text>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 white--text"
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<style scoped>
.v-card {
  width: 100%;
}
</style>

<script>
export default {
  data: () => ({
    icons: [
      {
        text: "mdi-github",
        link: "https://github.com/PasaYB/",
      },
      {
        text: "mdi-instagram",
        link: "https://instagram.com/pszaaaa/",
      },
    ],
  }),
};
</script>
