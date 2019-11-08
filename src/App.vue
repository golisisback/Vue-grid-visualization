<template>
  <v-app>
    <!-- Navigation drawer -->
    <v-navigation-drawer app color="white" v-model="drawer" temporary absolute>
      <v-card-text class="text-center">
        <v-toolbar-title>Nav Drawer</v-toolbar-title>
      </v-card-text>
    </v-navigation-drawer>

    <!-- App bar -->
    <v-app-bar app color="primary" dark>
      <v-card-text>
        <v-toolbar-title class="text-center">App Bar</v-toolbar-title>

        <!-- Button to open nav drawer -->
        <v-btn color="pink" dark @click.stop="drawer = !drawer">Open Me!</v-btn>
      </v-card-text>
    </v-app-bar>

    <!-- Main content -->
    <v-content class="purple lighten-3">
      <h2 class="text-center">&lt; Main Content Wrapper &gt;</h2>

      <!-- Container -->
      <v-container class="orange lighten-3" pa-5>
        <h3 class="text-center">Container (not fluid)</h3>

        <!-- V-row -->
        <v-row class="red lighten-1" justify="center">
          <v-col cols="12" class="red lighten-1">
            <h4 class="text-center">V-row</h4>
          </v-col>

          <!-- V-col -->
          <v-col cols="8" class="blue lighten-3" align="center">8 columns</v-col>
          <v-col cols="5" class="blue lighten-4" align="center">5 columns</v-col>
          <v-col cols="5" class="blue lighten-2" align="center">5 columns</v-col>
          <v-col cols="6" class="blue lighten-2" align="center">6 columns</v-col>
          <v-col cols="6" class="blue lighten-4" align="center">6 columns</v-col>
        </v-row>

        <br />

        <!-- V-col -->
        <v-row justify="center" class="red lighten-1">
          <v-col cols="4" class="blue lighten-2" align="center">4 columns</v-col>
          <v-col cols="4" class="blue lighten-4" align="center">4 columns</v-col>
          <v-col cols="4" class="blue lighten-2" align="center">4 columns</v-col>
          <v-col cols="3" class="blue lighten-4" align="center">3 columns</v-col>
          <v-col cols="3" class="blue lighten-2" align="center">3 columns</v-col>
          <v-col cols="3" class="blue lighten-4" align="center">3 columns</v-col>
          <v-col cols="6" class="blue lighten-3" align="center">6 columns</v-col>

          <v-col cols="12" class="red lighten-1">
            <h4 class="text-center">V-row</h4>
          </v-col>
        </v-row>
      </v-container>

      <br />
      <br />

      <!-- Container -->
      <v-container class="orange lighten-3" fluid pa-5="center">
        <h3 class="text-center">Container (fluid)</h3>

        <!-- V-row -->
        <v-row class="red lighten-1" justify="center">
          <v-col cols="12" class="red lighten-1">
            <h4 class="text-center">V-row</h4>

            <!-- Button to toggle color -->
            <v-btn color="green" dark align="center" @click="changeColor">Show/hide columns</v-btn>
          </v-col>

          <!-- V-col -->
          <v-col cols="3" id="id1" class="blue lighten-2" align="center">
            3 columns
            <v-row justify="center">
              <v-col cols="10">
                <v-card height="300px" align="center">V-card (300px width)</v-card>
              </v-col>
            </v-row>
          </v-col>

          <v-col cols="3" id="id2" class="blue lighten-4" align="center">
            3 columns
            <v-row justify="center">
              <v-col cols="8">
                <v-card height="300px" align="center">V-card (200px width)</v-card>
              </v-col>
            </v-row>
          </v-col>

          <v-col cols="3" id="id3" class="blue lighten-2" align="center">
            3 columns
            <v-row justify="center">
              <v-col cols="6">
                <v-card height="300px" align="center">V-card (100px width)</v-card>
              </v-col>
            </v-row>
          </v-col>

          <v-col cols="4" id="id4" class="blue lighten-4" align="center">
            4 columns
            <v-row id="id5" justify="center" class="red lighten-3" ma-4>
              V-row
              <v-col cols="6" id="id6" class="blue lighten-3">
                6 columns
                <v-card height="100px" align="center">V-card (100px height)</v-card>
              </v-col>
            </v-row>
          </v-col>

          <v-col cols="4" id="id7" class="blue lighten-2" align="center">
            4 columns
            <v-row justify="center">
              <v-col cols="6">
                <v-card height="200px" align="center">V-card (200px height)</v-card>
              </v-col>
            </v-row>
          </v-col>

          <v-col cols="4" id="id8" class="blue lighten-4" align="center">
            4 columns
            <v-row justify="center">
              <v-col cols="6">
                <v-card height="300px" align="center">V-card (300px height)</v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>

        <br />
      </v-container>

      <br />
      <br />
      <br />
      <br />
      <br />
    </v-content>

    <!-- Footer -->
    <v-footer absolute>
      <v-col align="center" cols="12">
        <strong>Footer</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: null,
    toggle: false
  }),
  methods: {
    changeColor() {
      if (this.toggle) {
        document.getElementById("id1").className = "blue lighten-2 col col-3";
        document.getElementById("id2").className = "blue lighten-4 col col-3";
        document.getElementById("id3").className = "blue lighten-2 col col-3";
        document.getElementById("id4").className = "blue lighten-4 col col-4";
        document.getElementById("id5").className = "red lighten-3";
        document.getElementById("id6").className = "blue lighten-3 col col-6";
        document.getElementById("id7").className = "blue lighten-2 col col-4";
        document.getElementById("id8").className = "blue lighten-2 col col-4";
      } else {
        document.getElementById("id1").className = "red lighten-1 col col-3";
        document.getElementById("id2").className = "red lighten-1 col col-3";
        document.getElementById("id3").className = "red lighten-1 col col-3";
        document.getElementById("id4").className = "red lighten-1 col col-4";
        document.getElementById("id5").className = "red lighten-1";
        document.getElementById("id6").className = "red lighten-1 col col-6";
        document.getElementById("id7").className = "red lighten-1 col col-4";
        document.getElementById("id8").className = "red lighten-1 col col-4";
      }
      this.toggle = !this.toggle;
    }
  }
};
</script>
