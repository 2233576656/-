<template>
  <div>
    <div class="inp"><el-input size="" prefix-icon="el-icon-edit" suffix-icon="el-icon-search" v-model="input" placeholder="请输入内容"></el-input></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: ''
    }
  }
};
</script>

<style lang="scss" scoped>
.inp {
  width: 450px;
  height: 100%;
  // border: 1px solid red;
  display: flex;
  justify-items: center;
  // margin-left: 20px;
  align-items: center;
}
</style>