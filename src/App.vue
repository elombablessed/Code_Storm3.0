<template>
  <v-app>
    <v-app-bar
      app
      color="transparent"
      flat
    >
      <h3 style="font-family: Courier New !important;" class="glow hidden-sm-and-down">&lt;CodeStorm/&gt;</h3>
      <div class="d-flex align-center">
        <!-- <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Code Storm"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        /> -->

      </div>

      <v-spacer></v-spacer>
      <Info 
        title="Mission" 
        titleMore="Our Mission" 
        completeInfo="Lorem ipsum dolor sit amet, consectetur adipiscing elit," 
        images="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"
      />
      <Info 
        title="Vision" 
        titleMore="Our Vission" 
        completeInfo="Lorem ipsum dolor sit amet, consectetur adipiscing elit," 
        images="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"
      />
      <Info 
        title="Objectives" 
        titleMore="Our Objectives" 
        completeInfo="Lorem ipsum dolor sit amet, consectetur adipiscing elit," 
        images="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"
      />
    </v-app-bar>

    <v-main class="pt-0">
      <Main />
    </v-main>
  </v-app>
</template>

<script>
import Main from './components/Main';
import Info from './components/Info';
// import Tabular from './components/Tabular'

export default {
  name: 'App',
  

  components: {
    Main,
    Info,
    // Tabular,
  },

  data: () => ({
    //
  }),
};
</script>

    <style>
      .glow {
        font-size: 30px;
        color: #ffffff;
        text-align: center;
        -webkit-animation: glow 1s ease-in-out infinite alternate;
        -moz-animation: glow 1s ease-in-out infinite alternate;
        animation: glow 1s ease-in-out infinite alternate;
      }
      @-webkit-keyframes glow {
        from {
          text-shadow: 0 0 5px #eeeeee, 0 0 10px #000000, 0 0 15px #000000, 0 0 40px #000000, 
                       0 0 25px #9554b3, 0 0 30px #9554b3, 0 0 45px #9554b3;
        }
        to {
          text-shadow: 0 0 10px #eeeeee, 0 0 15px #4d94ff, 0 0 40px #4d94ff, 0 0 50px #4d94ff,
                       0 0 30px #4d94ff, 0 0 45px #4d94ff, 0 0 80px #4d94ff;
        }
      }
    </style>