<template>
  <div class="container">
    <div class="wrapper">
      <h2>
        ルネサンス認定パーソナルトレーナーが「質の高いトレーニング」を提供します
      </h2>
      <div class="flex">
        <div class="flex-box">
          <img class="flex-img" src="@/img/top2_1.jpeg" alt="" />
          <h3>個別の目的に合わせたメニュー作成</h3>
          <p>生活スタイルなどに合わせ、無理なく目標達成できるよう最適なプランをご提案します。</p>
        </div>
        <div class="flex-box">
          <img class="flex-img" src="@/img/top2_2.jpeg" alt="" />
          <h3>マンツーマンのトレーニング指導</h3>
          <p>姿勢やクセなどを分析し正しいフォームでトレーニングできるようご案内します。</p>
        </div>
        <div class="flex-box">
          <img class="flex-img" src="@/img/top2_3.jpeg" alt="" />
          <h3>生活習慣のアドバイス</h3>
          <p>トレーニング時以外の過ごし方やお食事内容・タイミングを具体的にご提案します。</p>
        </div>
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
  background-color: black;
  color: white;
  padding: 30px 40px;
  .wrapper {
      width: 100%;
      max-width: 1100px;
      margin: auto;
    .flex {
      display: flex;
      width: 100%;
      margin: 30px auto;
      .flex-box {
        margin: auto;
        padding: 20px;
        .flex-img {
          width: 100%;
          max-width: 300px;
          margin: 10px;
        }
      }
    }
  }
}
</style>
