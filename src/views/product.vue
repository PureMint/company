<template>
  <section class="product">
    <v-header></v-header>
    <el-row>
      <!-- 全网搜索 -->
      <el-col :span="24">
        <div class="search" id="search">
          <div class="contentBox">
            <div class="text" style="top:260px;left:50px; margin-right: 177px;">
              <p>全网搜索</p>
              <div>
                输入公司名称，即可搜索项目工商，融资等多种信息；
              </div>
            </div>
            <div class="imgRight">
              <img src="/static/img/product/search-icon.png" alt="">
            </div>
          </div>
        </div>
      </el-col>
      <!-- 流程定制 -->
      <el-col :span="24">
        <div class="custom" id="custom">
          <div class="contentBox">
            <div class="text" style="top:260px;right:100px;margin-left:107px;">
              <p>流程定制</p>
              <div>
                根据机构业务定制流程，系统后台可快速配置；
              </div>
            </div>
            <div class="imgLeft">
              <img src="/static/img/product/custom-icon.png" alt="">
            </div>
          </div>
        </div>
      </el-col>
      <!-- 统计分析 -->
      <el-col :span="24">
        <div class="analyse" id="analyse">
          <div class="contentBox">
            <div class="text" style="top:260px;left:50px; margin-right: 177px;">
              <p>统计分析</p>
              <div>
                多角度报表统计分析，灵活的筛选条件，报表一键导出
              </div>
            </div>
            <div class="imgRight">
              <img src="/static/img/product/analyse-icon.png" alt="">
            </div>
          </div>
        </div>
      </el-col>
      <!-- 投后管理 -->
      <el-col :span="24">
        <div class="manage" id="manage">
          <div class="contentBox">
            <div class="text" style="top:260px;right:100px;margin-left:107px;">
              <p>投后管理</p>
              <div>
                自动跟踪项目动态，分析管理被投企业财务情况，业务数据
              </div>
            </div>
            <div class="imgLeft">
              <img src="/static/img/product/manage-icon.png" alt="">
            </div>
          </div>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="file" id="file">
          <div class="contentBox">
            <div class="text" style="top:260px;left:50px; margin-right: 177px;">
              <p>文档管理</p>
              <div>
                根据项目流程自动归档项目文档，灵活的项目配置权限
              </div>
            </div>
            <div class="imgRight">
              <img src="/static/img/product/file-icon.png" alt="">
            </div>
          </div>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="work" id="work">
          <div class="contentBox">
            <div class="text" style="top:260px;right:100px;margin-left:107px;">
              <p>协同办公</p>
              <div>
                机构同事间通过任务协作，记录每一项任务进程
              </div>
            </div>
            <div class="imgLeft">
              <img src="/static/img/product/work-icon.png" alt="">
            </div>
          </div>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="alarm" id="alarm">
          <div class="contentBox">
            <div class="text" style="top:260px;left:50px; margin-right: 177px;">
              <p>风险预警</p>
              <div>
                智能监控被投企业数据，第一时间自动预警
              </div>
            </div>
            <div class="imgRight">
              <img src="/static/img/product/alarm-icon.png" alt="">
            </div>
          </div>
        </div>
      </el-col>
    </el-row>
    <footer class="footer">
      <div @click="jumpHome">
        <p class="el-icon-arrow-up"></p>
        <p>返回首页</p>
      </div>
    </footer>
  </section>
</template>


<style lang="less" scoped>
  .product {
    margin-top: 70px;
    min-width: 1360px;
    .search {
      position: relative;
      height: 1080px;
      background: url(../../static/img/product/search-bg.png) no-repeat; // background-size: 100% 100%;
    }
    .custom {
      position: relative;
      height: 1080px;
      background: url(../../static/img/product/custom-bg.png) no-repeat;
      background-size: 100% 100%;
    }
    .analyse {
      position: relative;
      height: 1080px;
      background: url(../../static/img/product/analyse-bg.png) no-repeat;
      background-size: 100% 100%;
    }
    .manage {
      position: relative;
      height: 1080px;
      background: url(../../static/img/product/manage-bg.png) no-repeat;
      background-size: 100% 100%;
    }
    .file {
      position: relative;
      height: 1080px;
      background: url(../../static/img/product/file-bg.png) no-repeat;
      background-size: 100% 100%;
    }
    .work {
      position: relative;
      height: 1080px;
      background: url(../../static/img/product/work-bg.png) no-repeat;
      background-size: 100% 100%;
    }
    .alarm {
      position: relative;
      height: 1080px;
      background: url(../../static/img/product/alarm-bg.png) no-repeat;
      background-size: 100% 100%;
    }
    .contentBox {
      position: absolute;
      left: 50%;
      top: 50%;
      margin-left: -560px;
      margin-top: -452px;
      width: 1120px;
      height: 903px;
    }
    .text {
      width: 310px;
      height: 340px;
      position: absolute;
      background: rgba(255, 255, 255, .4);
      padding: 50px 45px;
      color: #00727d;
      box-sizing: border-box;
      p {
        font-size: 36px;
      }
      div {
        font-size: 24px;
        box-sizing: border-box;
        margin-top: 60px;
      }
    }
    .imgRight {
      position: absolute;
      right: 100px;
      top: 150px;
      cursor: pointer;
      &:hover {
        transition: all 2s ease;
        transform: rotate(360deg) translate(50px, 100px) scale(1.2);
      }
    }
    .imgLeft {
      position: absolute;
      left: 0;
      top: 226px;
      cursor: pointer;
      &:hover {
        transition: all 2s ease;
        transform: rotate(-360deg) translate(50px, 100px) scale(1.2);
      }
    }
    .footer {
      height: 70px;
      display: flex;
      justify-content: center;
      background: #2A3142;
      div {
        width: 75px;
        height: 70px;
        padding: 15px 0;
        text-align: center;
        box-sizing: border-box;
        color: #fff;
        cursor: pointer;
      }
    }
  }
</style>


<script>
  import vHeader from '../components/productHeader'
  export default {
    methods: {
      jumpHome() {
        this.$router.push({ name: 'home' });
      }
    },
    components: {
      vHeader
    }
  }
</script>
