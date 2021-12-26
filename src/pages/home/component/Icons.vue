<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key='index'>
        <div class="icon" v-for='item of page' :key='item.id'>
          <div class="icon-img">
            <img
              class="icon-img-content"
              :src='item.imgUrl'
            />
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: "HomeIcons",
  data() {
    return {
      iconList: [
        {
          id: 1,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/36d99efa6f2aa91f1ec9d18ce57fd5e3.png',
          desc: '酒店套餐酒店套餐酒店套餐酒店套餐酒店套餐酒店套餐',
        },
        {
          id: 2,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/a9d33792bd961b1692638d86cf3e6b83.png',
          desc: '滑雪',
        },
        {
          id: 3,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/557ba25df01d7dbf1419b095a11d1319.png',
          desc: '温泉',
        },
        {
          id: 4,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/d706a4d71c57c53ee8863b75a7af30cf.png',
          desc: '名胜古迹',
        },
        {
          id: 5,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/c4c5c620f20535ff358788a508c20921.png',
          desc: '主题乐园',
        },
        {
          id: 6,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/ace59857fe268552aa556189953aa369.png',
          desc: '自然风光',
        },
        {
          id: 7,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/aba25fb84648c130561afa5398d3552a.png',
          desc: '动植物园',
        },
        {
          id: 8,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/1fe870f93ec9bf5e30c4305acdca1822.png',
          desc: '品牌馆',
        },
        {
          id: 9,
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/36d99efa6f2aa91f1ec9d18ce57fd5e3.png',
          desc: '再来一次',
        },
      ]
    }
  },
  computed: {
    pages() {
      const pages = [];
      this.iconList.forEach((item, index) =>{
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      })
      return pages;
    }
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';
.icons >>> .swiper-container {
  height: 0;
  padding-bottom: 50%;
}

.icon {
  position: relative;
  overflow: hidden;
  float: left;
  width: 25%;
  height: 0;
  padding-bottom: 25%;

  .icon-img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0.44rem;
    box-sizing: border-box;
    padding: 0.1rem;

    .icon-img-content {
      display: block;
      margin: 0 auto;
      height: 100%;
    }
  }

  .icon-desc {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: 0.44rem;
    line-height: 0.55rem;
    text-align: center;
    color: $darkTextColor;
    ellipsis();
  }
}
</style>
