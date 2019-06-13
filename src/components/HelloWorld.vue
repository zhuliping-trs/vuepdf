<template>
  <div class="hello">
   <!--本地-->
    <div style="margin-top: 10px">
        <p>本地</p>
        <button @click="check">点击</button>
        <button @click="checkLocal">点击一下</button>
    </div>
    <!--服务器-->
    <!-- <div style="margin-top: 30px">
        <p>服务器</p>
        <button @click="checkError">查看错误</button>
        <button @click="checkNormal">查看有效</button>
        <button @click="checkSuccess">查看服务器跨域返回流</button>
    </div> -->
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  },
  methods: {
    check() {
      window.open("/static/pdf/web/viewer.html");
    },
    checkLocal() {
      //          let url = '/static/pdf/web/demo.pdf'
      let url = "ceshi.pdf";
      window.open("/static/pdf/web/viewer.html?file=" + url+"&highname="+"开发环境,的");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
