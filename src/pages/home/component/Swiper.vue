<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
      },
      swiperList: [
        {
          id: '0001',
          imgUrl:
            'https://img1.qunarzz.com/sight/p0/2109/20/204e37770f73cd73a3.water.jpg_600x330_8d8df0f9.jpg',
        },
        {
          id: '0002',
          imgUrl:
            'https://img1.qunarzz.com/sight/p0/201302/28/ee994376f26a254fc8d65eac.jpg_600x330_9677b91a.jpg',
        },
      ],
    };
  },
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
  padding-bottom: 55%;
  background-color: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>
