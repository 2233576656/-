<template>
  <div  class="square">
    <div class="square1"><frame></frame></div>
    <div class="square2"><put_questions_o></put_questions_o></div>
  </div>
</template>

<script>
export default {
  components: {
    frame: () => import('./frame.vue'),
    put_questions_o: () => import('./put_questions_o.vue')
  }
}
</script>

<style>
.square {
  display: flex;
}
.square1 {
  width: 65%;
  height: 100%;
  border: 1px solid red;
}
.square2 {
  width: 35%;
  height: 100%;
  border: 1px solid red;
}
</style>