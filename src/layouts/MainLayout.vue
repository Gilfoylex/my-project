<template>
  <div>
    <el-row>
      <el-col :span="8" :offset="6" class="content-layout">
        <main-carousel></main-carousel>
        <article-intros></article-intros>
      </el-col>
      <el-col :span="4" class="side-layout">
      </el-col>
    </el-row>
  </div>
</template>

<script>
import MainCarousel from '../components/MainCarousel.vue'
import ArticleIntros from '../components/ArticleIntros.vue'

export default {
  name: 'MainLayout',
  components:{
    MainCarousel,
    ArticleIntros
  }
}
</script>

<style scoped>
  .content-layout {
    margin-top: 90px;
    /* background-color: black;
    height: 100px; */
    top: 0px;
  }
  .side-layout {
    margin-top: 90px;
    margin-left: 8px;
    float: left;
    background-color: black;
    height: 100px;
    top: 0px;
  }
</style>