<template>
  <div>
    <div class="title">热门推荐</div>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <img
        class="item-img"
        :src="item.imgUrl"
      />

      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </li>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  data() {
    return {
      recommendList: [
        {
          id: "0001",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1505/18/18ffcca94b1b7ca2.water.jpg_200x200_9b0d2dc4.jpg",
          title: "长恨歌",
          desc: "回眸一笑百媚生，六宫粉黛无颜色 ，七月七日长生殿，夜半无人私语时"
        },
        {
          id: "0002",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1602/53/53cf6caed9f9b9ee90.img.jpg_200x200_f5476a84.jpg",
          title: "华清宫",
          desc: "白居易的《长恨歌》讲述了唐玄宗与杨贵妃凄婉的爱情故事，而华清宫也因这段风流往事令人神往。华清宫是唐代封建帝王游幸的别宫。背山面渭，倚骊峰山势而筑，规模宏大，建筑壮丽，楼台馆殿，遍布骊山上下。白居易《骊宫高》诗曰：“高高骊山上有宫，朱楼紫殿三四重”。"
        },
        {
          id: "0003",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1508/c5/a017645d82ab89f271fdfb1bd6ecc2e0.water.jpg_200x200_2de772de.jpg",
          title: "秦岭野生动物园",
          desc: "秦岭野生动物园——西安市民的后花园。西安秦岭野生动物园位于秦岭北麓，终南之巅。"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2em;
}

.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;

  .item-img {
    width: 1.7rem;
    height: 1.7rem;
    padding: 0.1rem;
  }

  .item-info {
    flex: 1;
    padding: 0.1rem;
    min-width: 0;

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

    .item-button {
      line-height: 0.24rem;
      margin-top: 0.26rem;
      background: #ff9300;
      padding: 0.05rem;
      border-radius: 0.06rem;
      color: #fff;
    }
  }
}
</style>

