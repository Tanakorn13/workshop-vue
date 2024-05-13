<template>
  <v-card
    class="mx-auto"
    max-width="600"
    style="
      border: solid 2px red;
      border-radius: 10px;
      box-shadow: 10px 5px 5px red;
    "
  >
    <v-img
      src="../assets/low-angle-view-unrecognizable-muscular-build-man-preparing-lifting-barbell-health-club.jpg"
      height="250px"
    ></v-img>

    <v-card-title class="d-flex justify-center orange--text">
      Hobby
    </v-card-title>

    <v-card-actions>
      <v-btn color="orange lighten-2" text> Explore </v-btn>

      <v-spacer></v-spacer>

      <v-btn icon @click="show = !show">
        <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text class="d-flex align-center flex-column">
          <div class="d-flex align-center font-weight-semi-bold text-h5 mr-2">
            <v-icon>mdi-dumbbell</v-icon>
            <h6 class="ml-1 mr-3">Gym</h6>
          </div>
          <div class="d-flex align-center font-weight-semi-bold text-h5">
            <v-icon>mdi-controller</v-icon>
            <h6 class="ml-1">Game</h6>
          </div>
          <div class="d-flex align-center font-weight-semi-bold text-h5">
            <v-icon>mdi-headphones</v-icon>
            <h6 class="ml-1">Music</h6>
          </div>
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  name: "HobbyCard",
  data: () => ({
    show: false,
  }),
};
</script>

<style></style>
