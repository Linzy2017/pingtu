<template>
  <div class="home">
    <div class="theme"></div>
    <h1>点击拼图，开始游戏吧~</h1>
    <div class="selections">
      <div v-for="n in 5" :class="active"></div>
    </div>
    <div class="btnGroup">
      <div class="btnPrize"></div>
      <div class="btnRules"></div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default{
  data () {
    return {
      completenun: []
    }
  }
}
</script>

<style lang="scss">
.home{
  @mixin show-background($path){
    background: url($path) no-repeat;
    background-size: 100%;
  }
  .theme {
    width: 4.85rem;
    height: 2.75rem;
    margin: 0.45rem auto 0.3rem;
    @include show-background("./theme.png");
  }
  h1{
    font: {
      size : 0.3rem;
      weight: 600;
    }
    text-align: center;
    color: rgb(158,88,34);
  }
  .selections{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 5.2rem;
    height: 4rem;
    margin: 0.14rem auto 0;
    padding-top: 0.25rem;
    background: rgb(241,230,176);
    border-radius: 0.5rem;
    box-shadow: 0rem 0.06rem 0rem 0.16rem rgb(217, 186, 162),
                inset 0rem 0.17rem 0rem 0.17rem rgb(236,216,162);
    > div{
      position: relative;
      left: 0.15rem;
      height: 1.8rem;
      &:first-child{
        width: 1.62rem;
        @include show-background("./4G.png");
      }
      &:nth-child(2){
        left: 0.25rem;
        width: 1.7rem;
        @include show-background("./flow.png");
      }
      &:nth-child(3){
        width: 1.8rem;
        @include show-background("./businessHall.png");
      }
      &:nth-child(4){
        width: 1.95rem;
        @include show-background("./roam.png");
      }
      &:nth-child(5){
        width: 1.95rem;
        @include show-background("./broadband.png");
      }
    }
  }
  .btnGroup{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 0.5rem;
    > div {
      width: 2.3rem;
      height:1rem;
    }
  }
  .btnPrize{
    margin-right: 0.4rem;
    background: url("./btnPrize.png") no-repeat;
    background-size: 100%;
  }
  .btnRules{
    background: url("./btnRule.png") no-repeat;
    background-size: 100%;
  }
}
</style>
