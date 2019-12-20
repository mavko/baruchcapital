<template light>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="float-left contentPane inverse">
          <div class="mt-6 mb-6">
            <logo />
          </div>
          <h1 style="color: #fff;"  class="mb-3">
            Welcome to Baruch Capital.
          </h1>
          <p style="color: #fff;" class="mb-6">
            A journal of sorts, detailing process, progress and musings regarding the financial markets.
          </p>
          <v-spacer />
          <v-btn nuxt to="/inspire">
            Langa pengar
          </v-btn>
          <no-ssr>
            <div>
              <div class="grid">
                <ChartBar />
                <ChartLine />
              </div>
            </div>
          </no-ssr>
      </div>
      <Header />
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Header from '~/components/Header.vue'
import ChartBar from "@/components/chart-bar";
import ChartDoughnut from "@/components/chart-doughnut";
import ChartLine from "@/components/chart-line";
export default {
  components: {
    Logo,
    Header,
    ChartBar,
    ChartDoughnut,
    ChartLine
  }
}
</script>

<style scoped>
@import "@/assets/variables.scss";
body {
    margin: 0;
    padding: 0;
    position: relative;
}
.boxBgTransparent p {
    max-width: 50%;
}
.contentPane {
    max-width: 1092px;
    min-width: 760px;
    width: calc(100vw - 302px);
    margin: 0 auto;
}
.inverse {

    text-shadow: 0 2px 20px 

    rgba(0,0,0,.16);

}
</style>