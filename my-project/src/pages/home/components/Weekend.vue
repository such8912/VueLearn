<template>
  <div>
    <div class="title">周末去哪儿</div>
    <li
      style="list-style-type:none"
      class="item border-bottom"
      v-for="item of recommendList"
      :key="item.id"
    >
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl" />
      </div>

      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
      </div>
    </li>
  </div>
</template>

<script>
export default {
  name: "HomeWeekend",
  data() {
    return {
      recommendList: [
        {
          id: "0001",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/63/808c022b285a2c.jpg_r_640x214_ad984479.jpg",
          title: "兵马俑",
          desc:
            "回眸一笑百媚生，六宫粉黛无颜色 ，七月七日长生殿，夜半无人私语时"
        },
        {
          id: "0002",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg",
          title: "钟楼",
          desc:
            "白居易的《长恨歌》讲述了唐玄宗与杨贵妃凄婉的爱情故事，而华清宫也因这段风流往事令人神往。华清宫是唐代封建帝王游幸的别宫。背山面渭，倚骊峰山势而筑，规模宏大，建筑壮丽，楼台馆殿，遍布骊山上下。白居易《骊宫高》诗曰：“高高骊山上有宫，朱楼紫殿三四重”。"
        },
        {
          id: "0003",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1507/de/e6ba44d61894c0.jpg_r_640x214_847324d0.jpg",
          title: "华清宫",
          desc:
            "秦岭野生动物园——西安市民的后花园。西安秦岭野生动物园位于秦岭北麓，终南之巅。"
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

.item-img-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 33.9%;

  .item-img {
    width: 100%;
  }
}

.item-info {
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

