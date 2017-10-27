<template>
  <section id="product">
    <el-row id="main">
      <!-- 全网搜索 -->
      <el-col :span="24">
        <div class="page" id="search">
        </div>
      </el-col>
    </el-row>
  </section>
</template>


<style lang="less" scoped>
@import '../common/css/variable.less';

#product {
  width: 100%;
  overflow: hidden; // margin-top: 70px;
  // min-width: 1000px;
  #main {
    height: 2944px;
    top: 0;
    position: relative;
  }
  #search {
    position: relative;
    background: url(../../static/img/product/search-bg.png) no-repeat;
    background-size: 100% 100%;
  }
}
</style>


<script>
export default {
  created() {
    this.goTop();
    document.addEventListener('mousewheel', this.scrollFunc, false);
  },
  mounted() {
    this.pageShow();
  },
  methods: {
    goAnchor(selector, index) {
      var anchor = this.$el.querySelector(selector);
      document.body.scrollTop = anchor.offsetTop;
      document.documentElement.scrollTop = anchor.offsetTop;
    },
    jumpHome() {
      this.$router.push({ name: 'home' });
    },
    goTop() {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    },
    pageShow() {
      var product = document.getElementById("product");

      var main = document.getElementById("main");

      var total = document.body.clientHeight || document.documentElement.clientHeight;
      console.log(total);

      product.style.height = total + "px";

      var obj = document.getElementsByTagName("div");
      for (var i = 0; i < obj.length; i++) {
        if (obj[i].className == 'page') {
          obj[i].style.height = total + "px";
        }
      }
    },
    scrollFunc(event) {
      // let num = 0;
      event = event || window.event;
      // var product = document.getElementById("product");

      // var main = document.getElementById("main");

      // var total = document.body.clientHeight;
      // console.log(total);

      // product.style.height = total + "px";

      // var obj = document.getElementsByTagName("div");
      // for (var i = 0; i < obj.length; i++) {
      //   if (obj[i].className == 'page') {
      //     obj[i].style.height = total + "px";
      //   }
      // }
      // let distence = document.body.scrollTop;
      if (event.wheelDelta > 0) {
        // alert('向上滚动');
      } else if (event.wheelDelta < 0) {
        // alert('向下滚动');
      }
    },

  }
}
</script>
