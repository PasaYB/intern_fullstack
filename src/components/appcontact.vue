<template>
  <section class="pb-11" id="contact">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row justify="center">
            <v-col cols="10" sm="">
              <h1 class="bebas-neue-regular">Contact Me</h1>
              <h3 class="font-weight-light mt-6">
                <span class="mdi mdi-phone"></span>
                Phone: +62-821-1498-0303
              </h3>
              <h3 class="font-weight-light mt-4">
                <span class="mdi mdi-email-outline"></span>
                Email: lananggading.pasa@gmail.com
              </h3>
              <h3 class="font-weight-light mt-4">
                <span class="mdi mdi-map-marker"></span>
                Address: Grogolan, Umbulmartani, Ngemplak, Sleman, Yogyakarta
              </h3>
            </v-col>
          </v-row>
        </v-col>
      </v-row>  
    </v-container>
    <v-snackbar
        v-model="snackbar.enabled"
        timeout="3000"
        right
        top
        :color="snackbar.color"
    >
      {{ snackbar.text }}

      <template v-slot:action="{ attrs }">
        <v-btn
            text
            v-bind="attrs"
            @click="snackbar.enabled = false"
        >
          Fechar
        </v-btn>
      </template>
    </v-snackbar>
  </section>
</template>

<style scoped>
#contact {
  background-size: cover;
  background-position: center;
  height: 300px;
}
.bebas-neue-regular {
  font-family: "Bebas Neue", sans-serif;
  font-size: 40px;
}
</style>

<script>

export default {
  data: () => ({
    valid: true,
    lazy: false,
    snackbar: {
      enabled: false,
      text: '',
      color: ''
    }
  }),
  };
</script>
