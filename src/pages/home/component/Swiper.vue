<template>
  <div class="wrapper">    
    <swiper :options="swiperOption" v-if="showSwiper"><!-- 避免由空数组数据创建组件造成轮播首次显示第四张图 -->
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array,
  },
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
      },
    };
  },
  computed: {
    showSwiper() {
      return this.list.length
    }
  }
};
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 30%;
  background-color: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>
