<template>
  <section id="home">
    <v-parallax dark src="@/assets/img/bg10.jpg" height="750">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="6" xl="8">
              <h1 class="bebas-neue-regular mb-2">Introduction</h1>
              <h1 class="poppins-thin"> My name is Lanang Gading Pasa, Im a student from Vocation High School 2 Depok Sleman Yogyakarta</h1>
              <v-btn
                rounded
                outlined
                large
                dark
                @click="$vuetify.goTo('#profile')"
                class="poppins-thin mt-7"
              >
                Press to see more Profile
                <v-icon class="ml-2">mdi-arrow-down</v-icon>
              </v-btn>
            </v-col>
            <v-col cols="12" md="6" xl="4" class="hidden-sm-and-down"> </v-col>
          </v-row>
        </v-col>
      </v-row>
      <div class="svg-border-waves text-white">
        <v-img src="@/assets/img/borderWaves.svg" />
      </div>
    </v-parallax>
    <v-container fluid id="profile" class="mt-2">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="space-around">
            <v-col cols="12" class="text-center">
              <h1 class="bebas-neue-regular mb-6">My Skills</h1>
            </v-col>
            <v-col
              cols="12"
              sm="4"
              class="text-center"
              v-for="(profile, i) in profile"
              :key="i"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card
                  class="card"
                  shaped
                  rounded
                  :elevation="hover ? 10 : 4"
                  :class="{ up: hover }"
                >
                  <v-img
                    :src="profile.img"
                    max-width="100px"
                    class="d-block ml-auto mr-auto"
                    :class="{ 'zoom-efect': hover }"
                  ></v-img>
                  <h1 class="bebas-neue-regular2">{{ profile.title }}</h1>
                  <h4 class="font-weight-regular subtitle-1">
                    {{ profile.text }}
                  </h4>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      profile: [
        {
          img: require("@/assets/img/1.png"),
          title: "Web Development",
        },
        {
          img: require("@/assets/img/2.png"),
          title: "Database Management",
        },
        {
          img: require("@/assets/img/3.png"),
          title: "Critical Thinking",
        },
      ],
    };
  },
};
</script>

<style>

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}

.poppins-thin {
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  font-style: normal;
}

.bebas-neue-regular {
  font-family: "Bebas Neue", sans-serif;
  font-size: 70px;
}
.bebas-neue-regular2 {
  font-family: "Bebas Neue", sans-serif;
  font-weight: 100;
  font-size: 30px;
}
.font-weight-light {
  font-family: 'Nunito', sans-serif;
}

#home {
  background-position: right center;
  z-index: 0;
}
.svg-border-waves img {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  margin-bottom: -2px;
  z-index: -1;
}

.card {
  min-height: 300px;
  padding: 60px;
  transition: 0.5s ease-out;
}

.card .v-image {
  margin-bottom: 15px;
  transition: 0.75s;
}

.card h1 {
  margin-bottom: 10px;
}

.zoom-efect {
  transform: scale(1.1);
}

.up {
  transform: translateY(-20px);
  transition: 0.5s ease-out;
}
</style>

<style>
section {
  position: relative;
}
</style>
