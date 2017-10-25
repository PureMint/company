<template>
    <section class="home">
        <v-header></v-header>
        <el-row>
            <el-col :span="24">
                <div class="banner">
                    <el-carousel height="540px">
                        <el-carousel-item v-for="item in 4" :key="item">
                            <img src="/static/img/home/banner-1.png" class="img-responsive"></img>
                        </el-carousel-item>
                    </el-carousel>
                </div>
            </el-col>
            <el-col :span="24">
                <div class="special">
                    <p>系统特色</p>
                    <!-- <img src="/static/img/home/special-bg.png" class="img-responsive"></img> -->
                    <div class="search">
                        <!-- <img src="/static/img/home/search.png"></img> -->
                        <div style="text-align:left;">
                            <p>全网搜索</p>
                            <span>支持工商查询，安全高效</span>
                        </div>
                    </div>
                    <div class="custom">
                        <!-- <img src="/static/img/home/custom.png"></img> -->
                        <div style="text-align:left;">
                            <p>流程定制</p>
                            <span>机构业务定制，快速配置</span>
                        </div>
                    </div>
                    <div class="analyse">
                        <!-- <img src="/static/img/home/analyse.png"></img> -->
                        <div style="text-align:left;">
                            <p style="padding-left: 90px">统计分析</p>
                            <span>数据库支持，筛选灵活，一键导出</span>
                        </div>
                    </div>
                    <div class="alarm">
                        <!-- <img src="/static/img/home/alarm.png"></img> -->
                        <div style="text-align:left;">
                            <p>风险预警</p>
                            <span>智能监控，快速预警</span>
                        </div>
                    </div>
                    <div class="manage">
                        <!-- <img src="/static/img/home/manage.png"></img> -->
                        <div style="text-align:left;">
                            <p style="padding-left: 90px">投后管理</p>
                            <span>被投项目实时跟踪，分析被投企业数据</span>
                        </div>
                    </div>
                    <div class="file">
                        <!-- <img src="/static/img/home/file.png"></img> -->
                        <div style="text-align:left;">
                            <p>文档管理</p>
                            <span>根据项目流程，自动归档，灵活配置</span>
                        </div>
                    </div>
                    <div class="work">
                        <!-- <img src="/static/img/home/work.png"></img> -->
                        <div style="text-align:left;">
                            <p>协同办公</p>
                            <span>业务机构协调统筹，实时记录</span>
                        </div>
                    </div>
                </div>
            </el-col>
            <el-col :span="24">
                <div class="control">
                    <div class="title">
                        <p>周期化管控</p>
                    </div>
                    <div class="controlBox">
                        <ul class="controlContent">
                            <li>
                                <div class="icon1">
                                </div>
                                <div class="iconBox iconMu" style="text-align:right;">
                                    <p style="font-size:20px;margin-bottom:16px">募</p>
                                    <p style="font-size:18px;">LP协议签署 LP打款记录 基金备案</p>
                                </div>
                            </li>
                            <li style="justify-content:flex-end;">
                                <div class="icon2">
                                </div>
                                <div class="iconBox iconTou" style="text-align:left;">
                                    <p style="font-size:20px;margin-bottom:16px">投</p>
                                    <p style="font-size:18px;">云项目池 考察储备 立项会 项目DD</p>
                                </div>
                            </li>
                            <li>
                                <div class="icon3">
                                </div>
                                <div class="iconBox iconGuan" style="text-align:right;">
                                    <p style="font-size:20px;margin-bottom:16px">管</p>
                                    <p style="font-size:18px;">投后管理 基金运算</p>
                                </div>
                            </li>
                            <li style="justify-content:flex-end;">
                                <div class="icon4">
                                </div>
                                <div class="iconBox iconExit" style="text-align:left;">
                                    <p style="font-size:20px;margin-bottom:16px">退</p>
                                    <p style="font-size:18px;">项目退出 LP收益分配 项目分红</p>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </el-col>
            <el-col :span="24">
                <div class="display">
                    <div class="title">
                        <p>案例展示</p>
                    </div>
                    <div class="displayBox">
                        <div v-for="(item,index) in List" :key="item.index">
                            <img :src="item.urlList" class="img-responsive"></img>
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
.home {
    margin-top: 70px;
    min-width: 1360px;
    .img-responsive {
        display: inline-block;
        height: 100%;
        max-width: 100%;
    }
    .special {
        position: relative;
        padding-top: 90px;
        height: 707px;
        text-align: center;
        background: url(../../static/img/home/special-bg.png) no-repeat;
        background-size: 100% 100%;
        >p {
            font-size: @font-size-large;
            color: @color-background-nav;
        }
        >div {
            position: absolute;
            cursor: pointer;
            div {
                width: 180px;
                word-wrap: break-word;
                >p {
                    font-size: @font-size-medium;
                    color: @color-background-nav;
                }
                >span {
                    font-size: @font-size-small;
                    color: @font-color-describe;
                }
            }
        }
        .search {
            width: 84px;
            height: 84px;
            top: 18%;
            left: 24%;
            background: url(../../static/img/home/search-1.png);
            &:hover {
                background: url(../../static/img/home/search.png);
            }
            div {
                position: absolute;
                top: 24%;
                left: 128%;
            }
        }
        .analyse {
            width: 64px;
            height: 64px;
            top: 66%;
            left: 30%;
            background: url(../../static/img/home/analyse-1.png);
            &:hover {
                background: url(../../static/img/home/analyse.png);
            }
            div {
                position: absolute;
                top: 24%;
                left: -295%;
            }
        }
        .work {
            width: 88px;
            height: 88px;
            top: 71%;
            left: 48%;
            background: url(../../static/img/home/work-1.png);
            &:hover {
                background: url(../../static/img/home/work.png);
            }
            div {
                position: absolute;
                top: 12%;
                left: 115%;
            }
        }
        .manage {
            width: 88px;
            height: 88px;
            top: 14%;
            left: 63%;
            background: url(../../static/img/home/manage-1.png);
            &:hover {
                background: url(../../static/img/home/manage.png);
            }
            div {
                position: absolute;
                top: 45%;
                left: -210%;
            }
        }
        .file {
            width: 64px;
            height: 64px;
            top: 37%;
            left: 71%;
            background: url(../../static/img/home/file-1.png);
            &:hover {
                background: url(../../static/img/home/file.png);
            }
            div {
                position: absolute;
                top: 165%;
                left: -70%;
            }
        }
        .alarm {
            width: 89px;
            height: 89px;
            top: 69%;
            left: 68%;
            background: url(../../static/img/home/alarm-1.png);
            &:hover {
                background: url(../../static/img/home/alarm.png);
            }
            div {
                position: absolute;
                top: 105%;
                left: 7%;
            }
        }
        .custom {
            width: 67px;
            height: 67px;
            top: 42%;
            left: 35%;
            background: url(../../static/img/home/custom-1.png);
            &:hover {
                background: url(../../static/img/home/custom.png);
            }
            div {
                position: absolute;
                top: 24%;
                left: 128%;
            }
        }
    }
    .control {
        height: 692px;
        padding-top: 90px;
        background: url(../../static/img/home/control-bg.png) no-repeat;
        background-size: 100% 100%;
        .title {
            width: 100%;
            text-align: center;
            margin-bottom: 40px;
            p {
                font-size: 30px;
                color: #fff;
            }
        }
        .controlBox {
            display: flex;
            justify-content: center;
            .controlContent {
                width: 1200px;
                li {
                    position: relative;
                    display: flex;
                    margin-bottom: 47px;
                    padding: 0 58px;
                }
                .iconBox {
                    width: 424px;
                    height: 60px;
                    padding: 14px 26px;
                    background: @color-fill;
                    border: 1px solid @color-h-background;
                    border-radius: 20px;
                    p {
                        color: @font-color-widget;
                    }
                }
                .icon1 {
                    width: 75px;
                    height: 75px;
                    margin: 0 26px;
                    position: absolute;
                    left: 45%;
                    background: url(../../static/img/home/muIcon.png) no-repeat;
                    &:hover {
                        cursor: pointer;
                        background: url(../../static/img/home/muIcon-1.png) no-repeat;
                    }
                    &:hover+.iconMu {
                        transition: all .5s ease;
                        transform: translateY(-20px);
                    }
                }
                .icon2 {
                    width: 75px;
                    height: 75px;
                    margin: 0 26px;
                    background: url(../../static/img/home/touIcon.png) no-repeat;
                    &:hover {
                        cursor: pointer;
                        background: url(../../static/img/home/touIcon-1.png) no-repeat;
                    }
                    &:hover+.iconTou {
                        transition: all .5s ease;
                        transform: translateY(-20px);
                    }
                }
                .icon3 {
                    width: 75px;
                    height: 75px;
                    margin: 0 26px;
                    position: absolute;
                    left: 45%;
                    background: url(../../static/img/home/guanIcon.png) no-repeat;
                    &:hover {
                        cursor: pointer;
                        background: url(../../static/img/home/guanIcon-1.png) no-repeat;
                    }
                    &:hover+.iconGuan {
                        transition: all .5s ease;
                        transform: translateY(-20px);
                    }
                }
                .icon4 {
                    width: 75px;
                    height: 75px;
                    margin: 0 26px;
                    background: url(../../static/img/home/exitIcon.png) no-repeat;
                    &:hover {
                        cursor: pointer;
                        background: url(../../static/img/home/exitIcon-1.png) no-repeat;
                    }
                    &:hover+.iconExit {
                        transition: all .5s ease;
                        transform: translateY(-20px);
                    }
                }
            }
        }
    }
    .display {
        height: 530px;
        padding: 90px 0 84px 0;
        .title {
            width: 100%;
            text-align: center;
            margin-bottom: 40px;
            p {
                font-size: 30px;
                color: #2a3142;
            }
        }
        .displayBox {
            display: flex;
            justify-content: center;
            >div {
                width: 360px;
                height: 241px;
                margin-right: 30px;
                cursor: pointer; // box-shadow: 5px 5px 5px #888;
                box-shadow: 1px 1px 1px #888;
                &:hover {
                    transform: scale(1.1);
                }
            }
        }
    }
}
</style>


<script>
import vHeader from '../components/header'
import vFooter from '../components/footer'
export default {
    created() {
        this.goTop();
    },
    data() {
        return {
            List: [
                {
                    urlList: '/static/img/home/dingding.png'
                },
                {
                    urlList: '/static/img/home/dongfang.png'
                }, {
                    urlList: '/static/img/home/didi.png'
                }
            ]
        }
    },
    methods: {
        goTop() {
           document.body.scrollTop = 0; 
        }
    },
    components: {
        vHeader,
        vFooter
    }
}
</script>


<ul>

</ul>
