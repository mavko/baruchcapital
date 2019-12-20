<template>
  <div class="cardShadowMedium">
    <div class="card">
      <chartjs-doughnut
        :bind="true"
        :datasets="datasets"
        :labels="labels"
        :option="option"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      datasets: [
        {
          data: [30, 10, 30, 20],
          backgroundColor: ["#f36e60", "#ffdb3b", "#185190"],
          hoverBackgroundColor: ["#fbd2cd", "#fef5c9", "#d1e3f7"]
        }
      ],
      labels: ["Stocks", "Bonds", "Forex", "P2P"],
      option: {}
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