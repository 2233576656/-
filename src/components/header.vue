<template>
  <div>
    <div class="header">
      <loog></loog>
      <list></list>
      <search></search>
      <head_portrait class="heads"></head_portrait>
    </div>
  </div>
</template>

<script>
// function setTime(params, sj) {
//   let timer = null;
//   return function() {
//     if (timer) {
//       clearTimeout(timer)
//       timer = setTimeout(params, sj) 
//     } else {
//       timer = setTimeout(params, sj)
//     }
    
//   }
// }
export default {
  data() {
    return {
      // 大小
      clientWidths: "",
      // clientHeights: "",
    };
  },

  components: {
    loog: () => import("./loog.vue"),
    list: () => import("./list.vue"),
    search: () => import("./search.vue"),
    head_portrait: () => import('./head_portrait.vue')
  },

  mounted() {
  },
  methods: {
  },
};
</script>

<style>
.header {
  width: 100%;
  /* height: 30%; */
  /* border: 1px solid red; */
  display: flex;
  justify-content: space-around;
}
</style>