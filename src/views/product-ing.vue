<template>
    <section id="product">
        <!-- 导航栏 -->
        <header class="navbar">
            <div class="logo">
                <img src="/static/img/logo-2.png" alt="领投者" class="img-responsive" />
            </div>
            <nav class="menu">
                <ul>
                    <li v-for="(item,index) in navList" class="animated bounceIn" :key="item.index">
                        <a style="color:#2A3142" href="javascript:void(0)" @click="goAnchor(item.id)"> {{item.menu}} </a>
                    </li>
                </ul>
            </nav>
        </header>
        <el-row id="main">
            <!-- 全网搜索 -->
            <el-col :span="24">
                <div class="page" id="search">
                    <div class="contentBox">
                        <div class="text" style="top:260px;left:50px; margin-right: 177px;">
                            <p>全网搜索</p>
                            <div>
                                输入公司名称，即可搜索项目工商，融资等多种信息；
                            </div>
                        </div>
                        <div class="imgRight">
                            <img src="/static/img/product/search-icon.png" class="img-responsive" alt="">
                        </div>
                    </div>
                </div>
            </el-col>
            <!-- 流程定制 -->
            <el-col :span="24">
                <div class="page" id="custom">
                    <div class="contentBox">
                        <div class="text" style="top:260px;right:100px;margin-left:107px;">
                            <p>流程定制</p>
                            <div>
                                根据机构业务定制流程，系统后台可快速配置；
                            </div>
                        </div>
                        <div class="imgLeft">
                            <img src="/static/img/product/custom-icon.png" class="img-responsive" alt="">
                        </div>
                    </div>
                </div>
            </el-col>
            <!-- 统计分析 -->
            <el-col :span="24">
                <div class="page" id="analyse">
                    <div class="contentBox">
                        <div class="text" style="top:260px;left:50px; margin-right: 177px;">
                            <p>统计分析</p>
                            <div>
                                多角度报表统计分析，灵活的筛选条件，报表一键导出
                            </div>
                        </div>
                        <div class="imgRight">
                            <img src="/static/img/product/analyse-icon.png" class="img-responsive" alt="">
                        </div>
                    </div>
                </div>
            </el-col>
            <!--投后管理 -->
            <el-col :span="24">
                <div class="page" id="manage">
                    <div class="contentBox">
                        <div class="text" style="top:260px;right:100px;margin-left:107px;">
                            <p>投后管理</p>
                            <div>
                                自动跟踪项目动态，分析管理被投企业财务情况，业务数据
                            </div>
                        </div>
                        <div class="imgLeft">
                            <img src="/static/img/product/manage-icon.png" class="img-responsive" alt="">
                        </div>
                    </div>
                </div>
            </el-col>
            <!-- 文档管理 -->
            <el-col :span="24">
                <div class="page" id="file">
                    <div class="contentBox">
                        <div class="text" style="top:260px;left:50px; margin-right: 177px;">
                            <p>文档管理</p>
                            <div>
                                根据项目流程自动归档项目文档，灵活的项目配置权限
                            </div>
                        </div>
                        <div class="imgRight">
                            <img src="/static/img/product/file-icon.png" class="img-responsive" alt="">
                        </div>
                    </div>
                </div>
            </el-col>
            <!-- 协同办公 -->
            <el-col :span="24">
                <div class="page" id="work">
                    <div class="contentBox">
                        <div class="text" style="top:260px;right:100px;margin-left:107px;">
                            <p>协同办公</p>
                            <div>
                                机构同事间通过任务协作，记录每一项任务进程
                            </div>
                        </div>
                        <div class="imgLeft">
                            <img src="/static/img/product/work-icon.png" class="img-responsive" alt="">
                        </div>
                    </div>
                </div>
            </el-col>
            <!-- 风险预警 -->
            <el-col :span="24">
                <div class="page" id="alarm">
                    <div class="contentBox">
                        <div class="text" style="top:260px;left:50px; margin-right: 177px;">
                            <p>风险预警</p>
                            <div>
                                智能监控被投企业数据，第一时间自动预警
                            </div>
                        </div>
                        <div class="imgRight">
                            <img src="/static/img/product/alarm-icon.png" class="img-responsive" alt="">
                        </div>
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
@import '../common/css/variable.less';
header {
    width: 100%;
    height: 70px;
    position: fixed;
    top: 0;
    z-index: 9999;
    background: #f2f4f8;
    min-width: 1000px;
    overflow: hidden;
    .img-responsive {
        display: block;
        height: auto;
        max-width: 100%;
    }
    .logo {
        position: fixed;
        top: 9px;
        left: 50px;
    }
    ul {
        float: right; // width: 870px;
        /*padding-right: 100px;*/
        padding-left: 230px;
        /*min-width: 400px;*/
        overflow: hidden;
        >li {
            float: left;
            color: #2A3142;
            height: 70px;
            width: 110px;
            box-sizing: border-box;
            text-align: center;
            line-height: 70px;
            cursor: pointer;
            &:hover {
                background: rgba(200, 200, 200, 0.15);
                border-bottom: 2px solid @color-border; // color: @color-border;
            }
        }
    }
}

#product {
    width: 100%; // overflow: hidden;
    #main {
        // height: 2944px;
        top: 0;
        position: relative;
        #search {
            position: relative;
            background: url(../../static/img/product/search-bg.png) no-repeat;
            background-size: cover;
        }
        #custom {
            position: relative;
            background: url(../../static/img/product/custom-bg.png) no-repeat;
            background-size: cover;
        }
        #analyse {
            position: relative;
            background: url(../../static/img/product/analyse-bg.png) no-repeat;
            background-size: cover;
        }
        #manage {
            position: relative;
            background: url(../../static/img/product/manage-bg.png) no-repeat;
            background-size: cover;
        }
        #file {
            position: relative;
            background: url(../../static/img/product/file-bg.png) no-repeat;
            background-size: cover;
        }
        #work {
            position: relative;
            background: url(../../static/img/product/work-bg.png) no-repeat;
            background-size: cover;
        }
        #alarm {
            position: relative;
            background: url(../../static/img/product/alarm-bg.png) no-repeat;
            background-size: cover;
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
            top: 185px;
            cursor: pointer;
            &:hover {
                transition: all 1s ease;
                transform: rotate(10deg); // transform: rotate(45deg) translate(50px, 100px) scale(1.2);
            }
        }
        .imgLeft {
            position: absolute;
            left: 0;
            top: 226px;
            cursor: pointer;
            &:hover {
                transition: all 1s ease;
                transform: rotate(-10deg); // transform: rotate(-360deg) translate(50px, 100px) scale(1.2);
            }
        }
    }
    .footer {
        height: 70px;
        display: flex;
        justify-content: center;
        background: #2A3142;
        position: fixed;
        right: 30px;
        bottom: 50px;
        border-radius: 50%;
        font-size: 13px;
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
export default {
    created() {
        this.goTop();
        // document.addEventListener('mousewheel', this.scrollFunc, false);
    },
    mounted() {
        this.pageShow();
    },
    data() {
        return {
            navList: [
                {
                    menu: '全网搜索',
                    id: '#search'
                },
                {
                    menu: '流程定制',
                    id: '#custom'
                },
                {
                    menu: '统计分析',
                    id: '#analyse'
                },
                {
                    menu: '投后管理',
                    id: '#manage'
                },
                {
                    menu: '文档管理',
                    id: '#file'
                },
                {
                    menu: '协同办公',
                    id: '#work'
                },
                {
                    menu: '风险预警',
                    id: '#alarm'
                }
            ]
        }
    },
    methods: {
        goTop() {
            document.body.scrollTop = 0;
            document.documentElement.scrollTop = 0;
        },
        jumpHome() {
            this.$router.push({ name: 'home' });
        },
        goAnchor(selector) {
            var anchor = this.$el.querySelector(selector);
            document.body.scrollTop = anchor.offsetTop;
            document.documentElement.scrollTop = anchor.offsetTop;
        },
        pageShow() {
            let product = document.getElementById("product");
            let total = document.documentElement.clientHeight;
            product.style.height = total + "px";
            let obj = document.getElementsByTagName("div");
            for (let i = 0; i < obj.length; i++) {
                if (obj[i].className == 'page') {
                    obj[i].style.height = total + "px";
                }
            }
        },
        scrollFunc(event) {
            var main = document.getElementById("main");
            var step = document.documentElement.clientHeight;
            //如果不加时间控制，滚动会过度灵敏，一次翻好几屏
            var startTime = 0, //翻屏起始时间  
                endTime = 0,
                now = 0;

            // 滚动事件处理函数
            event = event || window.event;
            startTime = new Date().getTime();
            var delta = event.detail || (-event.wheelDelta);
            //mousewheel事件中的 “event.wheelDelta” 属性值：返回的如果是正值说明滚轮是向上滚动
            //DOMMouseScroll事件中的 “event.detail” 属性值：返回的如果是负值说明滚轮是向上滚动
            if ((endTime - startTime) < -1000) {
                if (delta > 0 && parseInt(main.offsetTop) > -(step * 3)) {
                    //向下滚动
                    now = now - step;
                    this.toPage(now);
                }
                if (delta < 0 && parseInt(main.offsetTop) < 0) {
                    //向上滚动
                    now = now + step;
                    this.toPage(now);
                }
                endTime = new Date().getTime();
            } else {
                event.preventDefault();
            }
        },
        toPage(distence) {
            // var  main = document.getElementById("main");
            //   setTimeout("main.style.top = distence + 'px';", 1000);
            main.style.top = distence + 'px';
            //javascript 实现动画效果
        }
    }
}
</script>

