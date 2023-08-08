<template>
  <v-layout>

    <v-app-bar elevation="1" v-if="display.mdAndUp">

      <v-row>
        <v-col cols="2">

        </v-col>

        <v-col>
          <v-btn class="font-weight-black font-weight-bold text-h5" variant="plain" size="large" to="/">

            {{ appTitle }}

          </v-btn>

        </v-col>

        <v-col class="text-right">
          <v-btn v-for="item in desktop" :key="item.title" variant="plain" size="large" :to="item.path">

            {{ item.title }}

          </v-btn>
        </v-col>

        <v-col cols="2">

        </v-col>
      </v-row>

    </v-app-bar>



    <v-bottom-navigation v-else grow>
      <v-btn v-for="item in mobile" :key="item.title" color="teal" :to="item.path">
        <v-icon>{{ item.icon }}</v-icon>
        {{ item.title }}
      </v-btn>
    </v-bottom-navigation>



    <v-main>
      <v-row  v-if="display.mdAndUp">
        <v-col cols="2">

        </v-col>

        <v-col>
          <router-view></router-view>
        </v-col>


        <v-col cols="2">

        </v-col>
      </v-row>


      <v-row  v-else>
        <v-col cols="1">

        </v-col>

        <v-col>
          <router-view></router-view>
        </v-col>


        <v-col cols="1">

        </v-col>
      </v-row>
    </v-main>

  </v-layout>
</template>

<script>

import { useDisplay } from 'vuetify'
import { ref } from 'vue'


export default {
  components: {

  },

  data() {
    const display = ref(useDisplay())

    return {
      appTitle: "코대감",
      sidebar: false,
      desktop: [
        { title: "일정", path: "/schedule" },
        { title: "보고서", path: "/report" },
        { title: "설정", path: "/setting" },
      ],


      mobile: [
        { title: "홈", path: "/", icon: "mdi-home-outline" },
        { title: "일정", path: "/schedule", icon: "mdi-school-outline" },
        { title: "보고서", path: "/report", icon: "mdi-bullhorn-outline" },
        { title: "설정", path: "/community", icon: "mdi-cog-outline" },

      ],
      display
    };
  },
}
</script>