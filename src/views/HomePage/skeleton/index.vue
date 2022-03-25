<template>
  <div class="mains">
      <div class="box_lis"><Box></Box></div>
      <div class="tag_lis"><tag></tag></div>
  </div>
</template>

<script>
export default {
    components: {
        Box: () => import('./Box.vue'),
        tag: () => import('./tag.vue'),
    }
}
</script>

<style>
.mains {
    width: 100%;
    display: flex;
}
.box_lis {
    width: 65%;
}
.tag_lis {
    width: 35%;
}
</style>