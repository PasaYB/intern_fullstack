<template>
  <section id="gif">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" sm="9" class="white--text text-right mt-15">
              <v-btn rounded outlined href="https://github.com/PasaYB" target="_blank" large color="white" class="mt-9">
                <v-icon class="mr-2">
                  mdi-github
                </v-icon>
               More on github
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#gif {
  background-image: url("~@/assets/img/git.png");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 300px;
}
#download .container,
#download .row {
  height: 100%;
}
</style>