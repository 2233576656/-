<template>
  <div class="tag">
      <div class="tag_t">
          <div class="tag_i">
            <div class="tag_home"><i class="el-icon-edit"></i><div>文章发布</div></div>
            <div class="tag_but"> <div v-for="(it, index) in icon" :key="index"><el-button type="primary" :icon="it.icon" circle></el-button><div>{{it.name}}</div></div> </div>
            <div class="tag_img"><img src="https://img0.baidu.com/it/u=3369761343,577525464&fm=253&fmt=auto&app=138&f=JPEG?w=800&h=500" alt=""></div>
            <div><el-button icon="el-icon-plus">开始创作</el-button></div>
          </div>
          <div><img src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Finews.gtimg.com%2Fnewsapp_match%2F0%2F5836945131%2F0.jpg&refer=http%3A%2F%2Finews.gtimg.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1650616635&t=db63865aac54edbde9031436316a02ee" alt=""></div>
      </div>
  </div>
</template>

<script>
let biao = [
    {id: 1, icon:'el-icon-edit', name: '文章', },
    {id: 1, icon:'el-icon-video-camera', name: '视频', },
    {id: 1, icon:'el-icon-data-analysis', name: '广场', },

]
export default {
    data() {
        return {
            icon: []
        }
    },
    mounted() {
        this.icons()
    },
    methods: {
        icons() {
            new Promise((resolve) => {
                resolve()
            }).then(
                () => {
                    this.icon = biao
                }
            )
        }
    }
}
</script>

<style>
.tag {
    /* width: 30%; */
    /* height: 100px; */
    /* border: 1px solid rgb(22, 20, 20); */
}
.tag_t {
    margin: 10px;
    /* width: 100%; */
    height: 600px;
    /* border: 1px solid red; */
    background: #F6F6F6;
    margin-top: 10px;
    border-radius: 10px;
    padding: 15px;
}
.tag_t img {
    width: 100%;
    margin-top: 20px;
}
.tag_i {
    width: 100%;
    height: 50%;
    /* border: 1px solid red; */
}
.tag_home {
    width: 100%;
    display: flex;
    /* border: 1px solid red; */
    justify-items: left;
    align-items: center;
}
.tag_but {
    /* border: 1px solid red; */
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin-top: 10px;
}
.tag_but div {
    width: 75px;
    display: block;
    text-align: center;
}
.tag_but .el-button {
    width: 50px;
    height: 50px;
}
.tag_img {
    width: 100%;
    height: 100px;
    padding: 5px 0px;
    /* border: 1px solid red; */
}
.tag_img img {
    width: 100%;
    height: 100%;
}
.el-button {
    width: 100%;
    margin-top: 20px;
}
</style>