<template>
  <div id="article-intros">
    <div class="collections">
    </div>
    <ul class="article-intro-list">
      <li class="article-intro" v-for="item in 20" :key="item">
        <a class="title">大家都问我，为什么过年不回家</a>
        <p calss="abstract">1、 马上就是农历新年了，春节是一个理所当然的，
          要回家的日子，因为，那是一个理所当然的，团圆的日子。 
          异乡工作的人抢着车票，身边的人都时时的讨论着小时候在自己的家过年是一个什...
        </p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ArticleIntros'
}
</script>

<style scoped>
  .article-intro-list {
    list-style: none;
    padding-left: 0px;
  }
  .title {
    font-size: 20px;
    font-weight: bold;
  }
</style>