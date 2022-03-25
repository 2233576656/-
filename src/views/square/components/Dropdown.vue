<template>
  <div>
      <el-dropdown>
  <span class="el-dropdown-link">
    <i class="el-icon-more"></i>
  </span>
  <el-dropdown-menu slot="dropdown">
    <!-- <el-dropdown-item>修改</el-dropdown-item> -->
    <el-dropdown-item>删除</el-dropdown-item>
    <!-- <el-dropdown-item></el-dropdown-item> -->
  </el-dropdown-menu>
</el-dropdown>
  </div>
</template>

<script>
export default {

}
</script>

<style>
 .el-dropdown-link {
    cursor: pointer;
    color: #409EFF;
  }
  .el-icon-arrow-down {
    font-size: 12px;
  }
</style>