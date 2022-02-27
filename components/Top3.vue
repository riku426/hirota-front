<template>
  <div class="container">
    <div class="box">
      <h2>こんな方におすすめ！</h2>
      <p>以下のような目的・目標をお持ちの方におすすめしています。</p>
      <div class="row-flex">
        <el-row :gutter="20" type="flex">
          <el-col :span="4"
            ><img class="grid-img" src="@/img/top3/top3_1.jpeg" alt="" />
            <p>ダイエット・ 減量をしたい方</p></el-col
          >
          <el-col :span="4"
            ><img class="grid-img" src="@/img/top3/top3_1.jpeg" alt="" />
            <p>生活習慣病の 予防・改善</p></el-col
          >
          <el-col :span="4"
            ><img class="grid-img" src="@/img/top3/top3_1.jpeg" alt="" />
            <p>肩こり・腰痛・ 関節痛の予防・改善</p></el-col
          >
          <el-col :span="4"
            ><img class="grid-img" src="@/img/top3/top3_1.jpeg" alt="" />
            <p>スポーツ パフォーマンスの向上</p></el-col
          >
          <el-col :span="4"
            ><img class="grid-img" src="@/img/top3/top3_1.jpeg" alt="" />
            <p>スポーツ障害の 予防・改善など</p></el-col
          >
        </el-row>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style lang="scss" scoped>
.container {
  background-color: rgb(230, 227, 227);
  text-align: center;
  width: 100%;
  h2 {
      padding-top: 40px;
      padding-bottom: 40px;
      margin: 0;
  }
  .row-flex {
      padding-top: 30px;
    margin: auto;
    .el-row {
      padding: 0 150px;
    }
    .el-col {
      margin: auto;
      border-radius: 4px;
      .grid-img {
        width: 100%;
        max-width: 200px;
      }
    }
  }
}
</style>
