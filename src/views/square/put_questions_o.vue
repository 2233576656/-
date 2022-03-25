<template>
  <div>
    <div class="put_questions_o">
      <div class="put_questions_o_zi">
        <i class="el-icon-circle-plus-outline" style="font-size: 15px" /> 提问
      </div>
      <div class="put_questions_o_img">
          <img src="https://img1.baidu.com/it/u=1330864915,3695743451&fm=253&fmt=auto&app=138&f=JPEG?w=499&h=281" alt="">
      </div>
      <div class="put_questions_o_text">
        <el-input
          type="textarea"
          :rows="2"
          placeholder="请输入内容"
          v-model="textarea"
        >
        </el-input>
      </div>
      <div>
          <el-button style="width:100%">默认按钮</el-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      textarea: "",
    };
  },
};
</script>

<style>
.put_questions_o {
  width: 100%;
  height: 400px;
  border: 1px solid red;
  border-radius: 10px;
}
.put_questions_o_zi {
  border: 1px solid red;
  text-indent: 15px;
  font-size: 18px;
  margin-top: 15px;
}
.put_questions_o_img img {
    width: 100%;
}
</style>