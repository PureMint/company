<template>
    <footer  class="navbar navbar-default">
        <div class="container">
            <div class="footer-footer-main">
                <div class="row">
                    <ul class="col-xs-10">
                        <li v-for="(item,index) in List" :key="item.index">
                            <a href=""> {{ item.li }} </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer-social">
                <a href="#">
                    <img  alt="">
                </a>
                <a href="#">
                    <img  alt="">
                </a>
            </div>
        </div>
    </footer>
</template>

<script type="text/ecmascript-6">
export default {
    data() {
        return {
            List: [
                { li: '移动端111111111111' },
                { li: '首页' },
                { li: '产品' },
                { li: '服务' },
                { li: '下载' },
                { li: '关于' }
            ],
            bottomList: [
                { li: '京 ICP 备11017824号-4&nbsp;|&nbsp;京 ICP 备11017824号-4' },
                { li: '京 ICP 备11017824号-4&nbsp;|&nbsp;京 ICP 备11017824号-4' },
            ]
        }
    }
}
</script>

<style lang="less" scoped>
  @import '../common/css/variable.less';
  footer {
      width: 100%;
    //   position: fixed;
    //   bottom: 0;
  }
  .navbar {
     background: @color-background-nav;
  }
  .footer-main {
    height: 80px;
    line-height: 80px;
    border-bottom: 1px solid @color-border;
    min-width: 400px;
  }
  .footer-social {
    height: 80px;
    line-height: 80px;
    min-width: 360;
    padding: 20px auto;
  }
  ul {
      display: flex;
     flex-direction: row;
     li {
         float: left;
     }
  }

  a>img {
     margin-right: 36px;
  }

  a {
    color: @color-border;
    font-size: 14px;
    padding: 0 10px;
  }
</style>