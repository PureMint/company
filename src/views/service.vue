<template>
  <section class="service">
    <el-row>
      <el-col :span="24">
        <div class="banner">
          <img src="../../static/img/service/banner.png" class="img-responsive" alt=""/>
          <!--遮罩层-->
          <div class="half-mask">
            <div class="text">
              <h3>服 务</h3>
              <p class="animated fadeInRight">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam assumenda beatae consequatur consequuntur dolore, eos eum fugiat ipsum mollitia perspiciatis, ratione, tempore vero voluptate. Aperiam eaque facere incidunt nihil optio.</p>
            </div>
          </div>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="exploit">
          <p>开发实施服务</p>
          <el-row>
            <el-col :span="17" push="4" pull="4">
              <div style="margin-bottom: 30px">
                <span style=" font-size: 30px;border-bottom:1px solid #f00;margin-bottom: 5px">标准开发实施</span>
                <span style="width: 30px;height: 30px;background: #f00;color: #fff;font-size: 20px">免费</span>
              </div>
              <el-row style="overflow: hidden">
                <el-col :span="16" style="flex-direction: column;display:flex">
                  <div></div>
                  <img src="../../static/img/service/secondary.png" class="img-responsive"
                       style="flex-direction: column" alt="">
                  <div class="shade"></div>
                  <img src="../../static/img/service/train.png" class="img-responsive" style="flex-direction: column"
                       alt="">
                  <div class=""></div>
                </el-col>
                <el-col :span="8">
                  <img src="../../static/img/service/deploy.png" class="img-responsive" alt="">
                  <div class=""></div>
                </el-col>
              </el-row>
            </el-col>
          </el-row>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="customization">
          <el-row>
            <el-col :span="20" :offset="4">
              <div style="margin-bottom: 40px">
                <span style=" font-size: 30px;border-bottom:1px solid #f00;margin-bottom: 5px">定制开发实施</span>
                <span style="width: 30px;height: 30px;background: #f00;color: #fff;font-size: 20px">可选</span>
              </div>
              <el-row>
                <el-col :span="12" class="custom-made">
                  <img src="../../static/img/service/customization1.png" class="img-responsive" alt="">
                  <div class="custom-text">
                    <p class="animated fadeInRight">
                      本服务针对特定需求较多的客户按照实际研发工作量收费。
</p>
                  </div>
                </el-col>
                <el-col :span="12" :push="3" class="custom-made">
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
            <p>   领投者拥有一支技术精湛的专业运维服务队伍，具备先进的技术服务水平及丰富的软件系统运维经验。配合服务热线、远程技术支持和先进的服务管理机制，实现股权投资管理系统巡检、故障修复、数据库平台的安装、配置系统升级、系统更新及系统优化、系统高可靠性维护、数据存储及备份、技术培训等，有效的地帮助客户实现股权投资管理系统的平稳运行。并且由产品开发人员直接提供帮助。我们努力做到第一时间响应，保证所有疑问或请求会在一个工作日内回复</p>
          </div>
          <!--遮罩层-->
          <div class="half-mask">
            <div class="warranty">
              <h3>质保售后服务（免费）</h3>
              <p>
                领头者所售标准系统及定制功能均提供6个月免费质保服务、
                提供7*12电话技术支持服务、7*12远程技术支持服务
              </p>
              <h3>保后运维服务（可选）</h3>
              <p>超过免费质保期后的产品支持服务，按年收费，年费率=系统总价*12%。提供7*12电话技术支持服务、7*12远程技术支持服务。</p>
            </div>
          </div>
        </div>
      </el-col>
    </el-row>
  </section>
</template>


<style lang="less" scoped>
  @import '../common/css/variable.less';

  .service {
    font-family: "microsoft yahei";
    margin-top: 70px;
    .img-responsive {
      display: inline-block;
      height: auto;
      max-width: 100%;
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
      color: #fff;
      padding-left: 80%;
      padding-top: 136px;
      > h3 {
        padding-bottom: 5px;
        border-bottom: 5px solid #f00;
        margin-bottom: 50px;
      }
    }
    .exploit {
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
        transition: all 0.3s linear;
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
        height:156px;
        position: absolute;
        top: 25%;
        left: 25%;
        color: #fff;
        font-size: 20px;
        padding-top: 10%;
        p {
          transition: all 0.15s linear;
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
        color:#fff;
        padding-left: 46px;
        > h3 {
          margin-bottom: 42px;
        }
        >p {
          margin-bottom: 49px;
        }
      }

    }
  }
</style>


<script>
  export default {}
</script>
