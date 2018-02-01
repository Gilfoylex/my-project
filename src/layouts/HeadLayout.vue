<template>
  <div>
    <el-row>
      <el-col :span="12" :offset="6" >
        <slot></slot>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'HeadLayout',
}
</script>

<style scoped>

</style>