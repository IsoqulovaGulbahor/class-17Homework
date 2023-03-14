<template>
  <div class="world-map">
    <img src="./world map.png" alt="world map" />
    <div class="world-map_1">
      <canvas ref="myChart"></canvas>
      <div class="uzb-map">
        <img src="./uzb-map.png" alt="uzb-map" />
        <div class="uzb-map_1">
          <p>
            O'zbekiston <br />
            Qit'a: Osiyo <br />
            Davlat: O'zbekiston <br />
            Poytaxti: Toshkent <br />
            Maydoni: 4489400 km 2 <br />
            Aholisi: 35432050 <br />
            <button type="button">Ma'lumotlar📖</button>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js/auto";
export default {
  mounted() {
    const ctx = this.$refs.myChart.getContext("2d");
    const myChart = new Chart(ctx, {
      type: "bar",
      data: {
        labels: ["Amerika", "Xitoy", "Rossiya", "Hindiston", "Yaponiya"],
        datasets: [
          {
            label: "Iqtisodiyoti rivojlanayotgan davlatlar",
            data: [22, 16, 14, 12, 10],
            backgroundColor: [
              "red",
              "pink",
              "lightpink",
              "lightyellow",
              "yellow",
            ],
            borderColor: [
              "rgba(255, 99, 132, 1)",
              "rgba(255, 99, 132, 1)",
              "rgba(255, 99, 132, 1)",
            ],
            borderWidth: 1,
          },
        ],
      },
    });
  },
};
</script>

<style scoped>
body {
  padding: 0;
  margin: 0;
}
.world-map {
  width: 1200px;
  height: 600px;
}
.world-map img {
  margin-top: 20px;
  margin-bottom: 30px;
}
.uzb-map {
  display: flex;
}
.uzb-map_1 {
  width: 500px;
  height: 400px;
  margin-top: 125px;
  background-color: rgb(154, 254, 254);
  border-radius: 20px;
  border: 2px solid rgb(255, 0, 43);
}
.uzb-map_1 p {
  margin: 30px;
  font-size: x-large;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.uzb-map_1 button {
  width: 300px;
  height: 40px;
  margin-top: 20px;
  background-color: rgb(0, 255, 255);
  border: 2px solid rgb(255, 0, 43);
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  cursor: pointer;
}
</style>
