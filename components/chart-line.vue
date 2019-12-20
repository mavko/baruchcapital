<template>
  <div class="cardShadowMedium">
    <div class="">
      <div class="btn-group btn-group-toggle pa-4 boxDividerBottom-1">
        <label
          v-for="(item, index) in btn"
          :key="index"
          :class="{ active: item.value == radio }"
          class="btn btn-success"
        >
          <input
            v-model="radio"
            :name="dataLabel"
            :value="item.value"
            type="radio"
            class="radioBtn"
          />
          {{ item.label }}
        </label>
      </div>
    </div>

    <div class="card-img-bottom">
      <chartjs-line
        :backgroundcolor="bgColor"
        :beginzero="beginZero"
        :bind="true"
        :responsive="true"
        :bordercolor="borderColor"
        :data="data[radio]"
        :datalabel="dataLabel"
        :labels="labels[radio]"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      bgColor: "#81894e",
      beginZero: true,
      borderColor: "#81894e",
      btn: [
        { label: "Today", value: "day" },
        { label: "This Week", value: "week" }
      ],
      data: {
        day: [1, 3, 5, 3, 1],
        week: [12, 14, 16, 18, 11, 13, 15]
      },
      dataLabel: "144%",
      labels: {
        day: [7, 14, 21, 28, 16],
        month: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug"]
      },
      radio: "day"
    };
  }
};
</script>

<style scoped>
.cardShadowMedium {
    display: block;
    height: 320px;
    width: 600px;
    background:
    #fff;
    border-radius: 4px;
    float: left;
    margin-top: 80px;
    box-shadow: 0 7px 14px 0
    rgba(60, 66, 87, 0.12), 0 3px 6px 0 rgba(0, 0, 0, 0.12);
}
.radioBtn {
background-color:
rgb(84, 105, 212);
height: 14px;
box-shadow:
rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0.12) 0px 1px 1px 0px, rgb(84, 105, 212) 0px 0px 0px 1px, rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0) 0px 0px 0px 0px,
rgba(60, 66, 87, 0.12) 0px 2px 5px 0px;
min-width: 14px;
width: 14px;
transform: translateY(2.07px);
}
.boxDividerBottom-1 {
    box-shadow: inset 0 -1px 
    #e3e8ee;
}
</style>