<template>
  <div class="recommend-wrap">
    <div v-for="item in recommends" class="recommend-wrap-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <p>{{item.title}}</p>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  // data() {
  //   return {
  //     recommends: {
  //       type: Array,
  //       default() {
  //         return [];
  //       }
  //     }
  //   }
  // }
  props: {
    recommends: {
      type: Array,
      default() {
        return []
      }
    }
  }
}
</script>

<style scoped>

.recommend-wrap {
  display: flex;
  text-align: center;
  padding: 10px 0;
  border-bottom: 10px solid #ececec;
}

.recommend-wrap-item {
  flex: 1;
}

.recommend-wrap-item img{
  width: 70px;
  height: 70px;
}

</style>
