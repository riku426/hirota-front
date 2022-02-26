<template>
  <div class="container">
    <div class="box">
      <h2>パーソナルトレーニングとは</h2>
      <div class="flex">
        <div class="box-small">
          <p>
            経験豊富なパーソナルトレーナーが、お客様のご希望に沿った最適なトレーニングプログラムをご提案しながら、マンツーマン指導から2・3人へのグループ指導まで、お客様のニーズにご対応させていただきます。決められた時間で行うので、集中してトレーニングできることはもちろん、トレーナーが1つ1つを確認しながら行うので、あなたのペースで効率よく取り組めることが特徴。「一人ではなかなか続けられない...」「トレーニングの実践までしっかりとサポートして欲しい。」という方にもおすすめです。
          </p>
        </div>
        <div class="box-small">
          <img
            class="box2-img"
            src="@/img/top.jpeg"
            alt=""
            width="100%"
            height="367.5"
          />
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
  text-align: center;
  width: 100%;
  background-color: rgb(240, 236, 236);
  .box {
    text-align: center;
    padding-bottom: 30px;
    width: 100%;
    .flex {
      width: 100%;
      max-width: 1300px;
      background-color: white;
      margin: 35px auto;
      display: flex;
      .box-small {
        margin: 10px;
        padding-bottom: 20px;
        text-align: left;
        width: 50%;
        .box2-img {
          width: 100%;
          max-width: 600px;
          height: 367.5px;
        }
      }
    }
  }
}
</style>
