<template>
  <div class="lists">
    <ul class="list">
      <li v-for="(it, index) in lists" :key="index" @click="paths(it.path)">{{ it.name }}</li>
    </ul>
  </div>
</template>

<script>
const list = [
  { id: 1, name: "首页", path: "/", skt: "" },
  { id: 1, name: "广场", path: "/square", skt: "" },
];
export default {
  data() {
    return {
      lists: [],
      
    };
  },
  //   computed() {},
  mounted() {
    this.list();
  },
  computed: {
    
  },
  methods: {
    paths(val) {
      this.$router.push(val)
    },
    list() {
      new Promise((resolve) => {
        setTimeout(() => {
          if (list) {
            resolve("成功");
          }
        }, 100);
      }).then(() => {
        this.lists.push(...list);
      });
    },
  },
};
</script>

<style  lang="scss" scoped>
.list {
  width: 200px;
  height: 100%;
  display: flex;
  list-style-type: none;
  // border: 1px solid red;
  justify-content: space-around;
  align-items: center;
}
.list li {
  font-weight: bold;
}
.list li:hover {
  color: aqua;
  transition: all 0.3s linear 0s;
}
@media only screen and (max-width: 600px) {
  .list {
  width: 100px;
  height: 100%;
  display: flex;
  list-style-type: none;
  border: 1px solid red;
  justify-content: space-around;
  align-items: center;
}
.list li {
  font-weight: bold;
}
.list li:hover {
  color: aqua;
  transition: all 0.3s linear 0s;
}
}
</style>