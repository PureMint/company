<template>
  <!--<nav class="nav">-->
    <!--<div class="footer-main">-->
      <!--<el-row :gutter="20">-->
        <!--<el-col :span="9" :offset="3">-->
          <!--<ul>-->
            <!--<li v-for="list in liList">-->
              <!--<a href=""> {{ list.li }} </a>-->
            <!--</li>-->
          <!--</ul>-->
        <!--</el-col>-->
        <!--<el-col :span="6">-->
          <!--<ul class="icon">-->
            <!--<li class="icon1"></li>-->
            <!--<li class="icon2"></li>-->
          <!--</ul>-->
        <!--</el-col>-->
      <!--</el-row>-->
    <!--</div>-->
    <!--<div class="footer-social">-->
      <!--<el-row :gutter="20">-->
        <!--<el-col :span="12" :offset="6">-->
          <!--<ul>-->
            <!--<li v-for="(bottom,index) in bottomList" :key="bottom.index"> {{ bottom.li }} </li>-->
          <!--</ul>-->
        <!--</el-col>-->
      <!--</el-row>-->
      <!--<el-row :gutter="20">-->
        <!--<el-col :span="6" :offset="6">111</el-col>-->
        <!--<el-col :span="6" :offset="6">222</el-col>-->
      <!--</el-row>-->
    <!--</div>-->
  <!--</nav>-->
  <el-row class="nav">
    <el-col class="footer-main">
      <el-row :gutter="20">
        <el-col :span="10" :offset="2">
          <ul>
            <li v-for="list in liList">
              <a href="#"> {{ list.li }} </a>
            </li>
          </ul>
        </el-col>
        <el-col :span="10" :offset="2">
          <ul class="icon">
            <li class="icon1"></li>
            <li class="icon2"></li>
          </ul>
        </el-col>
      </el-row>
    </el-col>

    <el-col class="footer-social">
      <el-row :gutter="20" class="records">
        <el-col :span="10" :offset="2">
          <a href="#">京ICP备11017824号-4   | 京ICP证130164号  |  北京市公安局朝阳分局备案编号：110105020000501</a>
        </el-col>
      </el-row>
      <el-row :gutter="20" class="network">
        <el-col :span="10" :offset="2">
          <a href="#">网络文化经营许可证京网文[2016]6173-844号  |  广播电视节目制作经营许可证（京）字第06990号</a>
        </el-col>
        <el-col :span="10" :offset="2">
          <a href="#">opyright © 2006-2017 unicorn独角兽</a>
        </el-col>
      </el-row>
    </el-col>
  </el-row>
</template>

<script type="text/ecmascript-6">
  import ElRow from "element-ui/packages/row/src/row";
  export default {
    components: {ElRow}, data() {
      return {
        liList: [
          {li: '移动端'},
          {li: '首页'},
          {li: '产品'},
          {li: '服务'},
          {li: '下载'},
          {li: '关于'}
        ],
        bottomList: [
          {li: '京 ICP 备11017824号-4   |&nbsp;京 ICP 备11017824号-4'},
          {li: '京 ICP 备11017824号-4   |&nbsp;京 ICP 备11017824号-4'},
        ]
      }
    }
  }
</script>

<style lang="less" scoped>
  @import '../common/css/variable.less';

  .nav {
    width: 100%;
    background: #2A3142;
    overflow: hidden;
    position:relative;
    bottom: 0;
    left: 0;
    .footer-main {
      height: 80px;
      line-height: 80px;
      border-bottom: 1px solid #3d4a5b;
      .icon {
        margin-top: 32px;
      }
      .icon1 {
        width: 21px;
        height: 18px;
        margin-right: 50px;
        background: url(../../static/img/home/weChat.png) no-repeat -1px -17px;
        &:hover {
          cursor: pointer;
          background: url(../../static/img/home/weChat.png) no-repeat -1px -35px;
        }
      }
      .icon2 {
        width: 21px;
        height: 18px;
        background: url(../../static/img/home/weChat.png) no-repeat -27px -35px;
        &:hover {
          cursor: pointer;
          background: url(../../static/img/home/weChat.png) no-repeat -27px -17px;
        }
      }
    }
    .footer-social {
      height: 80px;
      /*line-height: 40px;*/
      .records{
        line-height: 40px;
      }
      .network{
        line-height: 40px;
      }
    }
    ul {
      display: flex;
      flex-direction: row;
    }
    ul li {
      float: left;
    }
    a {
      color: #3d4a5b;
      font-size: 14px;
      padding: 0 20px;
    }
  }

</style>
