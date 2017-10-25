<template>
  <section class="download">
    <v-header></v-header>
    <!-- <el-row>
                <el-col :span="24">
                  <div class="banner"> -->
    <!-- <img src="../../static/img/download/banner.png" class="img-responsive" alt="" /> -->
    <!-- </div>
                </el-col>
              </el-row> -->
    <el-row>
      <el-col :span="24">
        <div class="banner">
          <img src="../../static/img/download/banner.png" class="img-responsive" alt="" />
        </div>
        <div class="app">
          <img src="../../static/img/download/official.png" class="img-responsive" alt="">
          <el-row :gutter="20">
            <el-col :span="14" class="ios">
              <img src="../../static/img/download/ios.png" class="img-responsive" alt="">
              <img src="../../static/img/download/android.png" class="img-responsive" alt="">
            </el-col>
            <el-col :span="10">
              <img src="../../static/img/download/qr_code.png" class="img-responsive" alt="">
            </el-col>
          </el-row>
        </div>
      </el-col>
      <el-col :span="24" class="map">
        <img src="../../static/img/about/contact-bg.png" class="img-responsive" alt="">
        <div class="contact">
          <p>联系我们</p>
          <el-row :gutter="20">
            <el-col :span="10" :offset="4" class="home">
              <el-row :gutter="10">
                <el-col :span="4">
                  <ul>
                    <li v-for="(home,index) in homeList" :key="home.index"> {{ home.li }} </li>
                  </ul>
                </el-col>
                <el-col :span="4">
                  <ul>
                    <li v-for="(product,index) in productList" :key="product.index"> {{ product.li }} </li>
                  </ul>
                </el-col>
                <el-col :span="4">
                  <ul>
                    <li v-for="(service,index) in serviceList" :key="service.index"> {{ service.li }} </li>
                  </ul>
                </el-col>
                <el-col :span="4">
                  <ul>
                    <li v-for="(about,index) in aboutList" :key="about.index"> {{ about.li }} </li>
                  </ul>
                </el-col>
                <el-col :span="4">
                  <ul>
                    <li v-for="(download,index) in downloadList" :key="download.index"> {{ download.li }} </li>
                    <li>
                      <img src="../../static/img/download/qr_code.png" alt="">
                    </li>
                  </ul>
                </el-col>
              </el-row>

            </el-col>
            <el-col :span="10" class="address">
              <ul  class="address">
                <li v-for="(address,index) in addressList" :key="address.index"> {{address.li }} </li>
              </ul>
            </el-col>
          </el-row>
        </div>
      </el-col>
    </el-row>
    <v-footer></v-footer>
  </section>
</template>

<style lang="less" scoped>
  .download {
    min-width: 540px;
    margin-top: 70px;
    .clear {
      clear: both;
    }
    .img-responsive {
      display: block;
      height: auto;
      max-width: 100%;
    }
    .banner {
      position: relative;
    }
    .app {
      position: absolute;
      top: 19%;
      left: 21%;
      width: 25%;
      img {
        margin-bottom: 20px;
      }
      .ios img:nth-child(1)  {
         margin-bottom: 35px;
      }
    }
    .map {
      position: relative;
    }
    .contact {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 10%;
      left: 0;
      overflow: hidden;
      p {
        font-size: 30px;
        color: #fff;
        text-align: center;
        margin-bottom: 50px;
      }
      .address li:first-child {
        margin-bottom: 10px;
      }
      ul {
        float: left;
        li:first-child {
          margin-bottom: 30px;
        }
        li {
          color: #ddd;
          font-size: 15px;
          margin-bottom: 10px;
        }
        li:focus {
          color: #1d90e6;
        }
      }
    }
  }
</style>

<script>
  import vHeader from '../components/header'
  import vFooter from '../components/footer'
  export default {
    data() {
      return {
        homeList: [
          { li: '首页' },
          { li: '系统特色' },
          { li: '周期化管控' },
          { li: '联系我们' }
        ],
        productList: [
          { li: '产品' },
          { li: '全网搜索' },
          { li: '流程定制' },
          { li: '统计分析' },
          { li: '投后管理' },
          { li: '文档管理' },
          { li: '协同办公' },
          { li: '风险预警' }

        ],
        serviceList: [
          { li: '服务' },
          { li: '首页' },
          { li: '系统特色' },
          { li: '周期化管控' },
          { li: '联系我们' }
        ],
        aboutList: [
          { li: '关于' },
          { li: '系统特色' },
          { li: '周期化管控' },
          { li: '联系我们' }
        ],
        downloadList: [
          { li: '下载' }
        ],
        addressList: [
          { li: '公司：陕西深度网路有限公司' },
          { li: '地址：陕西省西安市高新区高新二路、12号协同大厦1层G1-10' },
          { li: '热线：029-86687710' },
          { li: '官方网址：www.sdcto.cn' },
          { li: '工作时间：09:00-18:00(周一至周五)' }
        ]
      }
    },
    components: {
      vHeader,
      vFooter
    }
  }
</script>
