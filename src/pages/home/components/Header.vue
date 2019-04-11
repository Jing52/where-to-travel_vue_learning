<template>
  <div>
    <div class="header">
      <div class="header-left">back</div>
      <div class="header-input">输入城市/景点/游玩主题</div>
      <div class="header-right">city</div>
    </div>
  </div>
</template>

<script>
export default{
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display: flex
    line-height: 1.6rem
    background: #00bcd4
    color: #fff
    .header-left
      width: 1.84rem
      float: left
    .header-input
      flex: 1
      height: 1.3rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
    .header-right
      width: 1.84rem
      float: right
      text-align: center
</style>
