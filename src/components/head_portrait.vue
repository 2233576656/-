<template>
  <div>
    <div class="head">
      <!-- <div>登录</div> -->
      <el-dropdown>
        <span class="el-dropdown-link">
          <img
            src="https://img0.baidu.com/it/u=2216119779,653055386&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500"
            alt=""
            class="el-icon-arrow-down el-icon--right"
          />
        </span>
        <el-dropdown-menu placement="top-start"  slot="dropdown">
          <el-dropdown-item></el-dropdown-item>
          <el-dropdown-item v-for="(it, index) in list_in" :key="index" >{{ it.name }}</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
    </div>
  </div>
</template>

<script>
let list = [
  {id: 1, name: '个人主页', path: '', key: '', Disable: false},
  // {id: 1, name: '暂无', path: '', key: '', Disable: true},
  {id: 1, name: '退出登录', path: '', key: '', Disable: false},
]
export default {
  data() {
    return {
      list_in: ''
    }
  },
  mounted() {
    this.list()
    this.list_ins()
  },
  methods: {
    list_ins() {
      console.log(12);
    },
    async list() {
       this.list_in = await list
    }
  }
};
</script>

<style>
.head {
  width: 200px;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  /* border: 1px solid red; */
}
.head img {
  width: 40px;
  height: 40px;
}
.el-dropdown-link {
    cursor: pointer;
    color: #409EFF;
  }
  .el-icon-arrow-down {
    font-size: 12px;
  }
</style>