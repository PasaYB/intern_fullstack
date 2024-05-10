<template>
  <section id="about">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h1 class="bebas-neue-regular mb-5 mt-10">My Project</h1>
              <v-row>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/lrvl.png"
                    max-width="60px"
                    class="mr-6"
                  />
                  <p class="poppins-thin">
                    Laravel Project, create a Local Web starting from creating a Login Page, Migration: DB Query, DB Relationship, MySQL Store Procedure, and the final result is an LTE Admin Web Page
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/php3.png"
                    max-width="60px"
                    class="mr-6"
                  />
                  <p class="poppins-thin">
                    Local Web Library, create a Local Web Library using the PHP programming language
                  </p>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12" md="5" class="dd-none d-md-flex align-self-end">
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
.bebas-neue-regular {
  font-family: "Bebas Neue", sans-serif;
  font-size: 70px;
}
.poppins-thin {
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  font-size: 19px;
  font-style: normal;
}
#about {
  margin-bottom: 100px;
}
</style>
