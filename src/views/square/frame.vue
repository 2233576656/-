<template>
  <div>
    <div class="frame_i" v-for="(it, index) in data" :key="index">
      <div class="frame_tx">
        <div class="frame_t">
          <head_portrait :tupian="it.tx"></head_portrait>
          <div class="names">{{it.username}}</div>
        </div>
        <div class="xiao"><Dropdown></Dropdown></div>
      </div>
      <div class="frame_ao">
        {{ it.list }}
      </div>
      <div class="frame_zan">
        <div>{{ it.zan }} <i class="el-icon-thumb" />赞</div>
        <div><i class="el-icon-star-off"></i> 收藏</div>
        <div style="display: flex">
          <el-input
            v-model="input"
            prefix-icon="el-icon-edit"
            size="small"
            placeholder="请输入内容"
          ></el-input>
          <el-button size="small " type="primary" icon="el-icon-s-comment">评论</el-button
          >
        </div>
        <div><i class="el-icon-warning"></i> 举报</div>
      </div>
    </div>
  </div>
</template>

<script>
import head_portrait from "./components/head_portrait.vue";
var information = [
  {
    id: 1,
    tx: "https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png",
    username: "小小",
    list: "javascript为什么这么麻烦1",
    zan: 0,
    pd: true,
  },
  {
    id: 2,
    tx: "https://img1.baidu.com/it/u=3796593454,4087161325&fm=253&fmt=auto&app=138&f=JPEG?w=889&h=500",
    username: "小王",
    list: "javascript为什么这么麻烦2",
    zan: 0,
    pd: true,
  },
  {
    id: 3,
    tx: "https://img1.baidu.com/it/u=3071602955,913052376&fm=253&fmt=auto&app=138&f=JPEG?w=796&h=500",
    username: "小狗",
    list: "javascript为什么这么麻烦3",
    zan: 0,
    pd: true,
  },
];
//  
export default {
  data() {
    return {
      input: "",
      data: [],
    };
  },
  components: {
    head_portrait,
    Dropdown: () => import('./components/Dropdown.vue')
  },
  mounted() {
    this.information();
  },
  methods: {
    information() {
      let promise = new Promise((resolve) => {
        resolve();
      });
      promise.then(() => {
        this.data = information;
      });
    },
  },
};
</script>
// 
<style>
.frame_i {
  width: 100%;
  height: 300px;
  border: 1px solid rgb(27, 25, 25);
  margin-top: 20px;
  border-radius: 10px;
}
.frame_tx {
  width: 100%;
  height: 50px;
  /* border: 1px solid red; */
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* padding:0px 10px ; */
}
.frame_t {
  display: flex;
  align-items: center;
  margin-left: 20px;
}
.names {
  margin-left: 15px;
}
.xiao {
  margin-right: 25px;
}
.frame_ao {
  width: 100%;
  height: 200px;
  border: 1px solid red;
  text-indent: 24px;
  margin-top: 10px;
}
.frame_zan {
  display: flex;
  height: 40px;
  justify-content: space-around;
  align-items: center;
  font-size: 12px;
}
</style>