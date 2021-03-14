<template>
  <div>
    <section>
      <v-row justify="center" align="center">
        <v-col cols="12" sm="12" md="6">
          <p class="text-h4 font-weight-bold text-center text-md-left">
            Growth partner for small businesses
          </p>
          <p class="text-center text-md-left">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Laborum
            dignissimos minus minima illum eveniet natus beatae iure aperiam
            deserunt ex excepturi exercitationem, nobis quidem incidunt vitae
            reiciendis ea commodi adipisci.<br />
            <v-btn
              class="primary text-center text-md-left"
              large
              justify="center"
            >
              Get Early acess now
            </v-btn>
          </p>
        </v-col>
        <v-col cols="12" sm="12" md="6"
          ><v-img
            lazy-src="https://picsum.photos/id/11/10/6"
            src="https://picsum.photos/id/11/500/300"
          ></v-img>
        </v-col>
      </v-row>
    </section>
    <section>
      <v-row justify="center" align="center">
        <v-col cols="12" sm="12" md="12">
          <p class="text-h3 text-sm-center">
            growth partner for small businesses
          </p>
        </v-col>

        <v-col cols="6" sm="6" md="4" v-for="src in img" :key="src">
          <v-img :src="src" height=" 120px" contain></v-img>
        </v-col>
      </v-row>
    </section>
    <section>
      <v-row justify="center" align="center">
        <v-col cols="12" sm="12" md="12">
          <v-card class="mx-auto" max-width="344" elevation="12">
            <v-card-text>
              <div>Word of the Day</div>
              <p class="display-1 text--primary">el·ee·mos·y·nar·y</p>
              <p>adjective</p>
              <div class="text--primary">
                relating to or dependent on charity; charitable.<br />
                "an eleemosynary educational institution."
              </div>
            </v-card-text>
            <v-card-actions>
              <v-btn text color="teal accent-4" @click="reveal = true">
                Learn More
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <v-card
                v-if="reveal"
                class="transition-fast-in-fast-out v-card--reveal"
                style="height: 100%"
              >
                <v-card-text class="pb-0">
                  <p class="display-1 text--primary">Origin</p>
                  <p>
                    late 16th century (as a noun denoting a place where alms
                    were distributed): from medieval Latin eleemosynarius, from
                    late Latin eleemosyna ‘alms’, from Greek eleēmosunē
                    ‘compassion’
                  </p>
                </v-card-text>
                <v-card-actions class="pt-0">
                  <v-btn text color="teal accent-4" @click="reveal = false">
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col cols="8" sm="12" md="3">
          <v-btn color="success" large>get funding support</v-btn>
        </v-col>
      </v-row>
    </section>
    <section>
      <v-row justify="center" align="center">
        <v-col cols="12" sm="12" md="6">
          <v-img
            src="https://picsum.photos/350/165?random"
            contain
            class="grey darken-4"
          ></v-img
        ></v-col>
        <v-col cols="12" sm="12" md="6">
          <p class="text-h4 text-sm-center">
            growth partner for small businesses
          </p>
          <p class="subtitle-2">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Laborum
            dignissimos minus minima illum eveniet natus beatae iure aperiam
            deserunt ex excepturi exercitationem, nobis quidem incidunt vitae
            reiciendis ea commodi adipisci.
          </p>
        </v-col>
      </v-row>
    </section>
    <section>
      <v-row>
        <v-col cols="6" sm="12" md="6" v-for="k in 4" :key="k">
          <div>
            <v-card class="mx-auto" max-width="344">
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                height="200px"
              ></v-img>

              <v-card-title> Top western road trips </v-card-title>

              <v-card-subtitle> 1,000 miles of wonder </v-card-subtitle>

              <v-card-actions>
                <v-btn color="orange lighten-2" text> Explore </v-btn>

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
                    I'm a thing. But, like most politicians, he promised more
                    than he could deliver. You won't have time for sleeping,
                    soldier, not with all the bed making you'll be doing. Then
                    we'll go with that data file! Hey, you add a one and two
                    zeros to that or we walk! You're going to do his laundry?
                    I've got to find a way to escape.
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </div>
        </v-col>
      </v-row>
    </section>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    Logo,
    VuetifyLogo,
  },
  data() {
    return {
      reveal: false,
      img: [
        "https://picsum.photos/id/11/500/300",
        "https://picsum.photos/id/11/500/300",
        "https://picsum.photos/id/11/500/300",
        "https://picsum.photos/id/11/500/300",
        "https://picsum.photos/id/11/500/300",
        "https://picsum.photos/id/11/500/300",
      ],
    };
  },
};
</script>
<style>
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
}
section {
  margin-top: 2em;
  margin-bottom: 10em;
}
</style>
