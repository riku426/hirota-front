<template>
  <div class="container">
    <div class="header">
      <Header />
    </div>
    <div class="question">
      <div>
        <p>今日のアルコール摂取量は？</p>
        <el-select v-model="alchol" placeholder="飲酒量">
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          >
          </el-option>
        </el-select>
      </div>
      <div class="flag-button">
        <el-button @click="handleChart" type="warning"
          >１週間の飲酒量表示</el-button
        >
      </div>
    </div>
    <div v-if="chartFlag" class="content">
      <BarChart />
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      chartFlag: false,
      alchol: "",
      options: [
        {
          value: "1合未満",
          label: "1合未満",
        },
        {
          value: "1合以上2合未満",
          label: "1合以上2合未満",
        },
        {
          value: "2合以上3合未満",
          label: "2合以上3合未満",
        },
        {
          value: "3合以上4合未満",
          label: "3合以上4合未満",
        },
      ],
    };
  },
  methods: {
    handleChart() {
      this.chartFlag = true;
    },
  },
  mounted() {},
};
</script>

<style lang="scss" scoped>
.container {
  height: 700px;
  background-color: rgb(241, 237, 237);
  .question {
    margin: 10px;
    padding: 10px;
    .flag-button {
      text-align: right;
      margin-top: 30px;
    }
  }
}
</style>
