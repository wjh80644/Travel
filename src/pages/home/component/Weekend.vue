<template>
  <div>
    <div class="title">周末去哪里</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img" />
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "HomeWeekend",
  data() {
    return {
      recommendList: [
        {
          id: 1,
          imgUrl:
            "https://imgs.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg",
          title: "故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿",
          desc: "浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿",
        },
        {
          id: 2,
          imgUrl:
            "https://imgs.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg",
          title: "故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿",
          desc: "浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿",
        },
        {
          id: 3,
          imgUrl:
            "https://imgs.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg",
          title: "故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿",
          desc: "浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿",
        },
        {
          id: 4,
          imgUrl:
            "https://imgs.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg",
          title: "故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿",
          desc: "浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿",
        },
        {
          id: 5,
          imgUrl:
            "https://imgs.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg",
          title: "故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿",
          desc: "浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿",
        },
      ],
    };
  },
};
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
}

ul {
  margin: 0;
  padding: 0;
}

p {
  margin: 0;
}

.item-img-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 33.9%;
}

.item-img {
  width: 100%;
}

.item-info {
  padding: 0.1rem;

  .item-title {
    line-height: 0.54rem;
    font-size: 0.32rem;
    ellipsis();
  }

  .item-desc {
    line-height: 0.4rem;
    color: #ccc;
    ellipsis();
  }

}
</style>