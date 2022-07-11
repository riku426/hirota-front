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
        <el-button @click="handleChart(alchol)" type="primary"
          >１週間の飲酒量表示</el-button
        >
      </div>
    </div>
    <div v-if="chartFlag" class="content">
      <div class="chart">
        <BarChart />
      </div>
    </div>
    <el-dialog title="飲みすぎ注意" :visible.sync="disableDaialg" width="80%">
      <span>あなたは２日連続でお酒を飲んでいます。休肝日を作りましょう。</span>
      <span slot="footer" class="dialog-footer">
        <el-button @click="disableDaialg = false">キャンセル</el-button>
      </span>
    </el-dialog>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      disableDaialg: false,
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
    handleChart(alchol) {
      this.chartFlag = true;
      if (alchol === "3合以上4合未満") {
        this.disableDaialg = true;
      }
    },
  },
  mounted() {},
};
</script>

<style lang="scss" scoped>
.container {
  height: 750px;
  background: -webkit-linear-gradient(left, #F89174, #FFC778);
  .question {
    margin: 10px;
    padding: 10px;
    .flag-button {
      text-align: right;
      margin-top: 30px;
    }
  }
}

.chart {
  padding: 15px;
  margin: 15px;
  background-color: white;
}
</style>
