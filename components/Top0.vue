<template>
  <div class="container">
    <div class="box">
      <h4>
        認定資格をもつ専属トレーナーがお客様のご希望からいちばん最適なトレーニングプログラムを作成。
        シェイプアップやリハビリを兼ねたトレーニング等、さまざまなニーズに1対1の個別指導で対応します。
      </h4>
      <div class="small-box">
        <div>
          <p>
            ※複数名で受けられるセミパーソナルトレーニングもございます。セミパーソナルトレーニングには2名と3名があります。
            ご家族・ご友人と一緒にトレーニングする事で、楽しく効果的なトレーニングができます。
            ※ルネサンス会員の方向けサービス。お手頃価格でパーソナルトレーニングが受けられます。
          </p>
        </div>
        <div class="mini-box">
            <h3>＼会員の方はこちら／</h3>
            <el-button class="el-button" type="danger" round>Danger</el-button><br>
            <nuxt-link to=""><p class="link">＞パーソナルトレーニングWEB予約サービスについて</p></nuxt-link>
        </div>
        <img src="@/img/top.jpeg" class="small-img" alt="">
        <p class="red-color">2ヶ月完結型 週2回のパーソナルトレーニング登場。会員以外の方もOK!</p>
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
  text-align: center;
  padding-bottom: 50px;
  .box {
    margin: auto;
    width: 50%;
    .small-box {
      margin: auto;
      width: 80%;
      font-size: 12px;
      .mini-box {
          padding-top: 30px;
        .el-button {
            width: 250px;
        }
        .link {
            padding-top: 15px;
            font-size: 13px;
        }
      }
      .small-img {
          width: 570px;
          margin-top: 40px;
          border-radius: 8px;
      }
      .red-color {
          color: red;
      }
    }
  }
}
</style>
