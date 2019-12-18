<template>
  <v-app class="boxBgTransparent">
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-footer absolute class="font-weight-medium">
      <v-col class="text-center" cols="12">
        {{ new Date().getFullYear() }} —
        <strong>BC.</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js"
    };
  }
};
</script>

<style scoped>
@import "@/assets/variables.scss";
.boxBgTransparent {
    background-color: none !important;
    background: transparent !important;
}

</style>