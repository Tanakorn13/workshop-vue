<template>
  <div class="container">
    <v-row>
      <v-col cols="6">
        <v-card
          class="mx-auto"
          max-width="600"
          style="
            border: solid 2px red;
            border-radius: 10px;
            box-shadow: 10px 5px 5px red;
          "
        >
          <div class="d-flex justify-center">
            <v-avatar color="primary" size="200" style="margin-top: 20px">
              <v-img src="../assets/IMG_5286.jpg" height="200px"></v-img>
            </v-avatar>
          </div>

          <v-card-title class="d-flex justify-center orange--text">
            ธนากร พงค์ทองเมือง
          </v-card-title>

          <v-card-subtitle class="d-flex justify-center orange--text">
            หนุ่ม
          </v-card-subtitle>

          <v-card-actions>
            <v-btn color="orange lighten-2" text> Profile </v-btn>

            <v-spacer></v-spacer>

            <v-btn icon @click="show = !show">
              <v-icon>{{
                show ? "mdi-chevron-up" : "mdi-chevron-down"
              }}</v-icon>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="show">
              <v-divider></v-divider>

              <v-card-text>
                <div
                  class="d-flex justify-center align-center font-weight-semi-bold text-h5"
                >
                  <h6>
                    ชื่อ: ธนากร พงค์ทองเมือง <br />
                    ชื่อเล่น: หนุ่ม <br />
                    อายุ: 23 ปี <br />
                    คณะ: วิศวกรรมศาสตร์ สาขาวิศวกรรมคอมพิวเตอร์ <br />
                    มหาวิทยาลัย: มหาวิทยาลัยสงขลานครินทร์ <br />
                    <!-- งานอดิเรก: ฟังเพลง เล่นเกม เข้าฟิตเนส <br /> -->
                  </h6>
                </div>
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </v-col>
      <v-col cols="6"> <HobbyCard /> </v-col>
    </v-row>

    <!-- <HobbyView /> -->
  </div>
</template>

<script>
import HobbyCard from "@/components/Hobby.vue";
// import TestCard from "@/components/TestCard.vue";

export default {
  name: "MeView",
  data: () => ({
    show: false,
  }),
  components: { HobbyCard },
};
</script>

<style></style>
