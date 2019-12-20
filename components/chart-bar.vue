<template>
  <div class="cardShadowMedium">
    <div class="card-img-bottom">
      <canvas id="fooCanvas" count="2" />

      <chartjs-bar
        v-for="(item, index) in types"
        :key="index"
        :backgroundcolor="item.bgColor"
        :beginzero="beginZero"
        :bind="true"
        :bordercolor="item.borderColor"
        :data="item.data"
        :datalabel="item.dataLabel"
        :labels="labels"
        target="fooCanvas"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      beginZero: true,
      labels: ["Stocks", "FX", "Bonds", "Treasuries", "Gold", "CC", "P2P"],
      types: [
        {
          bgColor: "#de98ab",
          borderColor: "0c0306",
          data: [1, 3, 5, 7, 2, 4, 6],
          dataLabel: "Stocks"
        },
        {
          bgColor: "#98ddde",
          borderColor: "030c0c",
          data: [1, 5, 2, 6, 3, 7, 4],
          dataLabel: "FX"
        }
      ]
    };
  }
};
</script>

<style scoped>
.cardShadowMedium {
    display: block;
    height: 240px;
    width: 480px;
    background:
    #fff;
    border-radius: 4px;
    float: right;
    margin-top: 80px;
    box-shadow: 0 7px 14px 0
    rgba(60, 66, 87, 0.12), 0 3px 6px 0 rgba(0, 0, 0, 0.12);
}

</style>