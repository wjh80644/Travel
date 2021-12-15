<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    test
  </div>
</template>

<script>
import HomeHeader from './component/Header';
import HomeSwiper from './component/Swiper';

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
  },
};
</script>

<style></style>
