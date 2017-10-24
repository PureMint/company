<template>
    <section  class="service">
        <v-header></v-header>
        <el-row>
            <el-col  :span="24">
                <div  class="banner">
                    <img  src="../../static/img/service/banner.png"  class="img-responsive"  alt=""/>
                    <!--遮罩层-->
                    <div  class="half-mask">
                        <div>
                            <p  class="title">服务</p>
                            <p  class="text  animated  fadeInRight">
                                &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;领投者拥有一支专业的软件开发和维护团队，可以为客户提供优质的开发实施服务和售后运维服务。对每一个“股权投资管理系统”建设项目，领投者都提供相应的技术服务，包括免费的标准开发实施和系统质保运维服务，以及按照开发工作量计价的定制开发实施服务、按年收费的系统保后运维服务，客户均根据自身的系统建设需求进行选购。</p>
                        </div>
                        <div  class="serve_red">SERVE</div>
                    </div>

                </div>
            </el-col>
            <el-col  :span="24">
                <div  class="exploit">
                    <p>开发实施服务</p>
                    <el-row  :gutter="20">
                        <el-col  :span="16"  :offset="4">
                            <div  style="margin-bottom:  30px">
                                <span  class="norm">
                                    标准开发实施
                                      <span  class="gratis">免费</span>
                                </span>
                            </div>
                            <el-row  style="overflow:  hidden">
                                <el-col  :span="16"  style="flex-direction:  column;display:flex">
                                    <div  class="tb_mask"  data-text="二次开发  "  style="font-size:  30px;">
                                        <img  src="../../static/img/service/secondary.png"  class="img-responsive"
                                                  style="flex-direction:  column"  alt="">
                                        <!--<span  style="width:  200px;  font-size:  20px;position:  absolute;top:0;right:  0;z-index:  1000">基于标准系统不超过10%功能点的二次开发，可根据用户的特定需求灵活定制。</span>-->
                                    </div>

                                    <div  class="bt_mask  train"  data-text="使用培训">
                                        <img  src="../../static/img/service/train.png"  class="img-responsive"  style="flex-direction:  column"
                                                  alt="">
                                    </div>
                                </el-col>

                                <el-col  :span="8">
                                    <div  class="rl_mask  train"  data-text="系统部署">
                                        <img  src="../../static/img/service/deploy.png"  class="img-responsive"  alt="">
                                    </div>
                                </el-col>
                            </el-row>
                        </el-col>
                    </el-row>
                </div>
            </el-col>
            <el-col  :span="24">
                <div  class="customization">
                    <el-row  :gutter="20">
                        <el-col  :span="16"  :offset="4">
                            <div  style="margin-bottom:  40px">
                                <span  class="norm">
                                    定制开发实施
                                    <span  class="gratis">可选</span>
                                </span>
                            </div>
                            <el-row  :gutter="20"  style="display:  flex;  flex-direction:  row  ;flex-wrap:  nowrap">
                                <el-col  :span="12"  class="custom-made">
                                    <img  src="../../static/img/service/customization1.png"  class="img-responsive"  alt="">
                                    <div  class="custom-text">
                                        <p  class="animated  fadeInRight">
                                            本服务针对特定需求较多的客户按照实际研发工作量收费。
                                       </p>
                  </div>
                </el-col>
                <el-col :span="6" :offset="5" class="custom-made">
                  <img src="../../static/img/service/customization2.png" class="img-responsive" alt="">
                  <div class="custom-text">
                    <p>服务包含标准系统的所有服务并根据用户功能需求进行深度定制开发。</p>
                  </div>
                </el-col>
              </el-row>
            </el-col>
          </el-row>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="after">
          <img src="../../static/img/service/after_sale.png" class="img-responsive" alt=""/>
          <div class="serve">
            <h1>售后支持服务</h1>
            <p>
              &nbsp; &nbsp; &nbsp;领投者拥有一支技术精湛的专业运维服务队伍，具备先进的技术服务水平及丰富的软件系统运维经验。配合服务热线、远程技术支持和先进的服务管理机制，实现股权投资管理系统巡检、故障修复、数据库平台的安装、配置系统升级、系统更新及系统优化、系统高可靠性维护、数据存储及备份、技术培训等，有效的地帮助客户实现股权投资管理系统的平稳运行。并且由产品开发人员直接提供帮助。我们努力做到第一时间响应，保证所有疑问或请求会在一个工作日内回复</p>
          </div>
          <!--遮罩层-->
          <div class="half-mask">
            <div class="warranty">
              <h3>质保售后服务（免费）</h3>
              <p>
                领头者所售标准系统及定制功能均提供6个月免费质保服务、 提供7*12电话技术支持服务、7*12远程技术支持服务
              </p>
              <h3>保后运维服务（可选）</h3>
              <p>超过免费质保期后的产品支持服务，按年收费，年费率=系统总价*12%。提供7*12电话技术支持服务、7*12远程技术支持服务。</p>
            </div>
          </div>
        </div>
      </el-col>
    </el-row>

    <v-footer></v-footer>
  </section>
</template>

<style lang="less" scoped>
  @import '../common/css/variable.less';

  .service {
    font-family: "microsoft yahei";
    margin-top: 70px;
    min-width: 1360px;
    .serve_red {
      width: 161px;
      height: 40px;
      line-height: 40px;
      font-size: 23px;
      background: #F05E5E;
      color: #fff;
      text-align: center;
      position: absolute;
      top: 14%;
      right: -161px;
    }
    .gratis {
      width: 30px;
      height: 30px;
      background: #F05E5E;
      color: #fff;
      font-size: 29px
    }
    .norm {
      font-size: 30px;
      border-bottom: 1px solid #F05E5E;
      margin-bottom: 5px
    }
    .img-responsive {
      display: block;
      height: auto;
      width: 100%;
    }
    .banner {
      position: relative;
      overflow: hidden;
      margin-bottom: 90px;
    }
    img {
      position: relative;
    }
    .half-mask {
      .title {
        font-size: 30px;
        color: #fff;
        border-bottom: 4px solid #F05E5E;
        position: absolute;
        top: 136px;
        right: 48px;
        padding-bottom: 15px;
      }
      /*背景颜色（透明），高度，宽度，绝对定位，初始位置，过渡*/
      background-color: rgba(0, 0, 0, 0.6);
      height: 100%;
      width: 100%;
      position: absolute;
      top: 0;
      right: 50%;
      transition: right 200ms;
      padding-right: 48px;
      text-align: right;
    }
    div.half-mask:hover {
      padding-right: 48px;
      text-align: right;
      right: 0;
    }
    .text {
      color: #9aa9ca;
      position: absolute;
      top: 220px;
      right: 48px;
      width: 500px;
    }
    .exploit {
      .train {

      }

      /*从上到下遮罩*/
      .tb_mask {
        position: relative;
        overflow: hidden;
        text-align: center;
        line-height: 200px;
      }
      .tb_mask:after {
        position: absolute;
        left: 0;
        top: 0;
        /*display: block;*/
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        content: attr(data-text);
        transition: all 0.3s linear;
        transform: translateY(-100%);
        color: #FFF;
      }
      .tb_mask:hover:after {
        transform: translateY(0);
      }

      /*从右向左遮罩*/
      .rl_mask {
        position: relative;
        overflow: hidden;
        text-align: center;
        line-height: 410px;
      }
      .rl_mask:after {
        position: absolute;
        left: 0;
        top: 0;
        /*display: block;*/
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        content: attr(data-text);
        transition: all 0.3s linear;
        transform: translateX(100%);
        color: #000;
      }
      .rl_mask:hover:after {
        transform: translateX(0);
      }

      /*从下到上遮罩*/
      .bt_mask {
        position: relative;
        overflow: hidden;
        line-height: 248px;
      }
      .train {
        text-align: center;
        font-size: 30px;
        color: #2A3142;
      }
      .bt_mask:after {
        position: absolute;
        left: 0;
        top: 0;
        /*display: block;*/
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        content: attr(data-text);
        transition: all 0.3s ease;
        transform: translateY(100%);
        color: #000;
      }
      .bt_mask:hover:after {
        transform: translateY(0);
      }

      margin-bottom: 90px;
      overflow: hidden;
      .shade {
        /*背景颜色（透明），高度，宽度，绝对定位，初始位置，过渡*/
        z-index: 100;
        background-color: rgba(0, 0, 0, 0.5);
        height: 50%;
        width: 67%;
        position: absolute;
        top: -40%;
        left: 0;
        transition: top 200ms;
      }
      .shade:hover {
        top: 0;
      }
      > p {
        font-size: 30px;
        color: @font-color-title;
        text-align: center;
        margin-bottom: 90px;
        transition: all 0.15s linear;
      }
      p:hover {
        padding-left: 5%;
      }
      > .row > p {
        font-size: 30px;
        color: @font-color-title;
        text-align: left;
        margin-bottom: 30px;
      }
    }
    .customization {
      margin-bottom: 90px;
      img {
        transition: all 0.3s ease;
      }
      img:hover {
        transform: scale(1.1);
      }
      .custom-made {
        width: 524px;
        height: 312px;
        position: relative;
        overflow: hidden;
      }
      .custom-text {
        width: 262px;
        /*height: 156px;*/
        position: absolute;
        top: 30%;
        left: 25%;
        color: #fff;
        font-size: 20px;
        /*padding-top: 10%;*/
        p {
          transition: all 0.15s ease;
        }
        p:hover {
          padding-right: 5%;
        }
      }
    }
    .after {
      height: 600px;
      overflow: hidden;
      position: relative;
      .serve {
        position: absolute;
        left: 25%;
        top: 20%;
        text-align: right;
        width: 400px;
        h1 {
          transition: all 0.15s linear;
        }
        h1:hover {
          padding-right: 5%;
        }
        p {
          transition: all 0.15s linear;
        }
        p:hover {
          padding-right: 5%;
        }
      }
      .half-mask {
        /*背景颜色（透明），高度，宽度，绝对定位，初始位置，过渡*/
        background-color: rgba(0, 0, 0, 0.6);
        height: 100%;
        width: 100%;
        position: absolute;
        top: 0;
        left: 50%;
        transition: left 200ms;
        padding-right: 48px;
        text-align: left;
      }
      div.half-mask:hover {
        text-align: left;
        left: 0;
      }
      .warranty {
        padding-right: 80%;
        padding-top: 136px;
        color: #fff;
        padding-left: 46px;
        > h3 {
          margin-bottom: 42px;
        }
        > p {
          margin-bottom: 49px;
        }
      }
    }
  }
</style>


<script>
  import vHeader from '../components/header'
  import vFooter from '../components/footer'
  export default {
    components: {
      vHeader,
      vFooter
    }
  }
</script>