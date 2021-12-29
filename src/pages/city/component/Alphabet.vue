<template>
  <ul class="list">
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
  </ul>
</template>
<script>
export default {
  name: 'CityAlphabet'
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .list {
    display: flex;
    flex-direction: column;
    justify-content: center
    position: absolute;
    top: 1.58rem;
    right: 0;
    bottom: 0;
    width: .4rem;
    .item {
      line-height: .4rem;
      text-align: center;
      color: $bgColor
    }
  }
</style>