<template>
  <div class="box_1">
    <div class="box" v-for="(it, index) in a" :key="index">
      <div class="box_i">
        <h4 ref="appsss" id="usename">{{ it.name }}</h4>
      </div>
      <div class="box_list" ref="usenames" v-show="it.judge == true" >
        {{ it.list }}
      </div>
      <div class="box_list" v-show="it.judge == false">
        {{ it.list }}
      </div>
      <div class="box_zan">
        <div>
          <el-tag>{{ it.zan }} <i class="el-icon-thumb"></i>赞</el-tag>
        </div>
        <div>
          <el-tag><i class="el-icon-s-comment"></i>评论</el-tag>
        </div>
        <div>
          <el-tag><i class="el-icon-star-off"></i>收藏</el-tag>
        </div>
        <div>
          <el-tag><i class="el-icon-info"></i> 举报</el-tag>
        </div>
        <div>
          <el-tag @click="open(it)"
            >{{ it.message }} <i :class="it.el_icon"></i
          ></el-tag>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
let list = [
  {
    id: 1,
    name: "javascript信息管理从入门到入土1",
    list: 'JavaScript是运行在浏览器上的脚本语言。简称JS。JavaScript是网景公司（NetScape)的 布兰登·艾奇 开发的，最初叫做LiveScript。LiveScript的出现让浏览器更加生动，使得页面更具有交互性。JavaScript（简称“JS”） 是一种具有函数优先的轻量级，解释型或即时编译型的编程语言。虽然它是作为开发Web页面的脚本语言而出名的，但是它也被用到了很多非浏览器环境中，JavaScript 基于原型编程、多范式的动态脚本语言，并且支持面向对象、命令式和声明式（如函数式编程）风格。JavaScript在1995年由Netscape公司的Brendan Eich，在网景导航者浏览器上首次设计实现而成。因为Netscape与Sun合作，Netscape管理层希望它外观看起来像Java，因此取名为JavaScript。但实际上它的语法风格与Self及Scheme较为接近。JavaScript和java没有任何关系，只是语法类似。JavaScript运行在浏览器中，代码由浏览器解释后执行。而Java运行在JVM中。JavaScript的“目标程序”以普通文本形式保存，这种语言都叫做"脚本语言“。Java的目标程序已.class形式存在，不能使用文本编辑器打开，不是脚本语言。1998年网景公司由“美国在线”公司收购。王景公司最著名的就是“领航者浏览器”：Navigator浏览器。LiveScript的出现，最初的时候是为Navigator浏览器量身定制一门语言，不支持其他浏览器。微软一看不行，研发了只支持IE浏览器的脚本语言。JScript。在两者语言共存的时代，程序员需要写两套程序。这时一个叫做ECMA组织（欧洲计算机协会）根据JavaScript制定了ECMA-262标准，叫做ECMA-Script.JavaScript是一种属于网络的脚本语言,已经被广泛用于Web应用开发,常用来为网页添加各式各样的动态功能',
    zan: 0,
    message: "展开",
    judge: true,
    el_icon: "el-icon-arrow-down",
  },
  {
    id: 2,
    name: "javascript信息管理从入门到入土2",
    list: 'JavaScript是运行在浏览器上的脚本语言。简称JS。JavaScript是网景公司（NetScape)的 布兰登·艾奇 开发的，最初叫做LiveScript。LiveScript的出现让浏览器更加生动，使得页面更具有交互性。JavaScript（简称“JS”） 是一种具有函数优先的轻量级，解释型或即时编译型的编程语言。虽然它是作为开发Web页面的脚本语言而出名的，但是它也被用到了很多非浏览器环境中，JavaScript 基于原型编程、多范式的动态脚本语言，并且支持面向对象、命令式和声明式（如函数式编程）风格。JavaScript在1995年由Netscape公司的Brendan Eich，在网景导航者浏览器上首次设计实现而成。因为Netscape与Sun合作，Netscape管理层希望它外观看起来像Java，因此取名为JavaScript。但实际上它的语法风格与Self及Scheme较为接近。JavaScript和java没有任何关系，只是语法类似。JavaScript运行在浏览器中，代码由浏览器解释后执行。而Java运行在JVM中。JavaScript的“目标程序”以普通文本形式保存，这种语言都叫做"脚本语言“。Java的目标程序已.class形式存在，不能使用文本编辑器打开，不是脚本语言。1998年网景公司由“美国在线”公司收购。王景公司最著名的就是“领航者浏览器”：Navigator浏览器。LiveScript的出现，最初的时候是为Navigator浏览器量身定制一门语言，不支持其他浏览器。微软一看不行，研发了只支持IE浏览器的脚本语言。JScript。在两者语言共存的时代，程序员需要写两套程序。这时一个叫做ECMA组织（欧洲计算机协会）根据JavaScript制定了ECMA-262标准，叫做ECMA-Script.JavaScript是一种属于网络的脚本语言,已经被广泛用于Web应用开发,常用来为网页添加各式各样的动态功能',
    zan: 0,
    message: "展开",
    judge: true,
    el_icon: "el-icon-arrow-down",
  },
  {
    id: 3,
    name: "javascript信息管理从入门到入土3",
    list: 'JavaScript是运行在浏览器上的脚本语言。简称JS。JavaScript是网景公司（NetScape)的 布兰登·艾奇 开发的，最初叫做LiveScript。LiveScript的出现让浏览器更加生动，使得页面更具有交互性。JavaScript（简称“JS”） 是一种具有函数优先的轻量级，解释型或即时编译型的编程语言。虽然它是作为开发Web页面的脚本语言而出名的，但是它也被用到了很多非浏览器环境中，JavaScript 基于原型编程、多范式的动态脚本语言，并且支持面向对象、命令式和声明式（如函数式编程）风格。JavaScript在1995年由Netscape公司的Brendan Eich，在网景导航者浏览器上首次设计实现而成。因为Netscape与Sun合作，Netscape管理层希望它外观看起来像Java，因此取名为JavaScript。但实际上它的语法风格与Self及Scheme较为接近。JavaScript和java没有任何关系，只是语法类似。JavaScript运行在浏览器中，代码由浏览器解释后执行。而Java运行在JVM中。JavaScript的“目标程序”以普通文本形式保存，这种语言都叫做"脚本语言“。Java的目标程序已.class形式存在，不能使用文本编辑器打开，不是脚本语言。1998年网景公司由“美国在线”公司收购。王景公司最著名的就是“领航者浏览器”：Navigator浏览器。LiveScript的出现，最初的时候是为Navigator浏览器量身定制一门语言，不支持其他浏览器。微软一看不行，研发了只支持IE浏览器的脚本语言。JScript。在两者语言共存的时代，程序员需要写两套程序。这时一个叫做ECMA组织（欧洲计算机协会）根据JavaScript制定了ECMA-262标准，叫做ECMA-Script.JavaScript是一种属于网络的脚本语言,已经被广泛用于Web应用开发,常用来为网页添加各式各样的动态功能',
    zan: 0,
    message: "展开",
    judge: true,
    el_icon: "el-icon-arrow-down",
  },
];
export default {
  data() {
    return {
      a: [],
      
      
      tr: true,
    };
  },
  mounted() {
    this.list();
  },
  updated() {
    this.$nextTick(() => {
      let i = this.$refs.appsss;
      let a = this.$refs.usenames;
      if (this.tr == true) {
        i.forEach((it) => {
          it.innerHTML.length > 16
            ? (it.innerHTML = it.innerHTML.slice(0, 16) + "...")
            : it;
        });
        a.forEach((it) => {
          it.innerHTML.length > 250
            ? (it.innerHTML = it.innerHTML.slice(0, 250) + "...")
            : it;
        });
      } else if (this.tr == false) {
        console.log(i, a);
      }
    });
  },
  methods: {
    list() {
      new Promise((resolve) => {
        resolve();
      }).then(() => {
        this.a.push(...list);
      });
    },
    open(val) {
      let thia = this;
      var ar = thia.$refs.usenames;
      // this.tr = false
      // thia.tr = false;
      // console.log(1222);
      if (val.id) {
         if (val.message == "展开") {
          // var arr = ''
          val.message = "收回";
          val.judge = false
          val.el_icon = "el-icon-arrow-up";
          return console.log(ar[val.id - 1], 1);
        } else if (val.message == "收回") {
          // var arr = ''
          console.log(2);
          val.message = "展开";
          val.judge = true
          val.el_icon = "el-icon-arrow-down";
          return console.log(ar[val.id - 1]);
        }
        return
      }
    },
  },
};
</script>

<style>
.box {
  width: 100%;
  /* border: 1px solid rgb(185, 187, 177); */
  background: #f6f6f6;
  border-radius: 10px;
  /* height: 100px; */
  margin-top: 10px;
}
.box_i {
  width: 250px;
  /* height: 35px; */
  /* border: 1px solid red; */
  text-align: center;
  margin-left: 2.5%;
}
.box_list {
  /* height: 100px; */
  width: 92%;
  margin: 0 auto;
  /* border: 1px solid red; */
  text-indent: 24px;
  font-size: 15px;
  padding: 10px;
}
.box_zan {
  width: 95%;
  height: 40px;
  /* border: 1px solid red; */
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-around;
}
</style>