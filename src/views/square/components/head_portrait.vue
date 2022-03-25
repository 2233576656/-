<template>
  <div>
    <div>
      <el-avatar :src="tupian"></el-avatar>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tupian: {
      type: String,
      default: "",
    },
  },
  mounted() {
  },
};
</script>

<style>
</style>