<template>
  <div>
    <el-row>
      <el-col :span="8" :offset="6" class="content-layout">
        <test></test>
        <slot name="carousel"></slot>
        <slot name="articles"></slot>
      </el-col>
      <el-col :span="4" class="side-layout">
      </el-col>
    </el-row>
  </div>
</template>

<script>
import test from '../components/test.vue'

export default {
  name: 'MainLayout',
  components:{
    test
  }
}
</script>

<style scoped>
  .content-layout {
    margin-top: 90px;
    /* background-color: black;
    height: 100px; */
  }
  .side-layout {
    margin-top: 90px;
    margin-left: 10px;
    background-color: black;
    height: 100px;
  }
</style>