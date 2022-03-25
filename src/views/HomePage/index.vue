<template>
  <div class="home">
    <skeleton></skeleton>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
      skeleton: () => import('./skeleton/index.vue')
  }
}
</script>

<style lang="scss" scoped>
.home {
  
}
</style>
