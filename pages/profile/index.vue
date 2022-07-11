<template>
  <div class="container">
    <div class="header">
      <Header />
    </div>
    <div class="content">
      <p>あなたの身長は？</p>
      <el-input placeholder="身長" v-model="height" class="input"></el-input>
      <p>あなたの体重は？</p>
      <el-input placeholder="体重" v-model="weight" class="input"></el-input>
      <p>あなたの拡張期血圧は？</p>
      <el-input placeholder="血圧" v-model="blood" class="input"></el-input>
      <p>あなたの空腹時血糖は？</p>
      <el-input placeholder="血糖値" v-model="suger" class="input"></el-input>
      <p>あなたの好きなビールのタイプは？</p>
      <el-select v-model="beer" placeholder="好きなビール" class="input">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        >
        </el-option>
      </el-select>
    </div>
    <div class="beer-button">
      <el-button type="primary" @click="handleBeer" class="recomend-btn"
        >あなたにおすすめのビールを見る</el-button
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      height: "",
      weight: "",
      blood: "",
      suger: "",
      beer: "",
      options: [
        {
          value: "コクがある",
          label: "コクがある",
        },
        {
          value: "フルーティー",
          label: "フルーティー",
        },
        {
          value: "味が濃い",
          label: "味が濃い",
        },
        {
          value: "苦味がある",
          label: "苦味がある",
        },
      ],
    };
  },
  methods: {
    handleBeer() {
      this.$router.push({path: "/drink", query: {option: this.beer}});
    },
  },
};
</script>


<style lang="scss">
.container {
  height: 750px;
  background: -webkit-linear-gradient(left, #F89174, #FFC778);
  .beer-button {
    margin-top: 20px;
    text-align: right;
  }
}

.input {
  width: 70%;
  margin: 10px;
}
.recomend-btn {
  margin-bottom: 15px;
}
</style>