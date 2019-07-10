<template>
  <div>
    <div class="title">周末去哪儿</div>
    <li
      style="list-style-type:none"
      class="item border-bottom"
      v-for="item of list"
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
  props:{
    list : Array
  }
  
};
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2em;
}

.item-img-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 37.09%;

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

