<template>
  <ul class="list">
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
  </ul>
</template>

<script>
export default {
  name: 'CityAlpahbet'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
    .list
      position: absolute
      top: 1.58rem
      right: 0
      bottom: 0
      width: .4rem
      display: flex
      flex-direction: column
      justify-content: center
      .item
        color: #000
        text-align: center
        line-height: .4rem
        color: $bgColor
</style>
