<template light>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-center mt-6 mb-6">
        <logo />
      </div>
      <v-card class="contentPane" light>
        <v-card-title class="headline">
          Welcome to Baruch Capital. 
        </v-card-title>
        <v-card-subtitle>
          This is the personal page of its propriotor Sebastian Selling, 
          a Malta-based, Swedish-born, visual designer by trade, turned swing trader and investor. 
          <br>
          This is his journal, detailing process, progress and musings on his projects and life in general.
        </v-card-subtitle>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/inspire">
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style scoped>
@import "@/assets/variables.scss";
</style>