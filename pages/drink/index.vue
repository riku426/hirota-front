<template>
  <div class="container">
    <div class="header">
      <Header />
    </div>
    <div class="content">
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
      <p>ビールの産地は？</p>
      <el-input placeholder="国名" v-model="contry" class="input"></el-input>
      <p>ビールの価格帯は？</p>
      <el-input placeholder="下限" v-model="lowPrice" class="money"></el-input
      ><span>〜</span
      ><el-input placeholder="上限" v-model="highPrice" class="money"></el-input>
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
      beer: "",
      contry: '',
      lowPrice: '',
      highPrice: '',
      options: [
        {
          value: "コクがある",
          label: "コクがある",
        },
        {
          value: "キレがある",
          label: "キレがある",
        },
        {
          value: "フルーティ",
          label: "フルーティ",
        },
        {
          value: "麦芽感が強い",
          label: "麦芽感が強い",
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
      this.$router.push({ path: "/drink/recomend", query: { option: this.beer } });
    },
  },
};
</script>


<style lang="scss">
.container {
  height: 750px;
  background: -webkit-linear-gradient(left, #f89174, #ffc778);
  .beer-button {
    margin-top: 20px;
    text-align: right;
  }
}

.input {
  width: 70%;
  margin: 10px;
}
.money {
  width: 40%;
  margin: 10px;
}
.recomend-btn {
  margin-bottom: 15px;
}
</style>