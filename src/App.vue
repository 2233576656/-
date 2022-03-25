<template>
  <div id="app">
    <headers></headers>
    <router-view class="view"/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      clientWidths: "",
    }
  },
  components: {
    headers: () => import('./components/header.vue')
}
}
</script>


<style>
* {
  padding: 0;
  margin: 0px;
}
.view {
  width: 80%;
  /* height:calc(100vh - 80px); */
  border: 1px solid red;
  margin: 0 auto;
}
</style>
