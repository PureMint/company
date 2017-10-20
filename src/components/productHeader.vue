<template>
    <header class="navbar">
        <div class="logo">
            <img src="/static/img/logo.png" alt="领投者" class="img-responsive"/>
        </div>
        <nav class="menu">
            <ul>
                <li v-for="(item,index) in navList" class="animated bounceIn" :key="item.index" @click="jump(index)">
                    {{item.menu}}
                </li>
            </ul>
        </nav>
    </header>
</template>


<style lang="less" scoped>
@import '../common/css/variable.less';
body {
    width: 100%;
    position: relative;
}
header {
    width: 100%;
    height: 70px;
    position: fixed;
    top: 0;
    z-index: 9999;
    background: transparent;
    border-bottom: 1px solid #fff;
    .logo {
        position: fixed;
        top: 9px;
        left: 50px;
    }
    @media screen and (min-width:1080px) {
        ul {
            float: right;
            padding-right: 100px;
            >li {
                float: left;
                color: #fff;
                height: 70px;
                width: 110px;
                box-sizing: border-box;
                text-align: center;
                line-height: 70px;
                cursor: pointer;
                &:hover {
                    background: rgba(225, 225, 225, 0.15);
                    border-bottom: 2px solid @color-border;
                    color: @color-border;
                }
            }
        }
    }
    @media screen and (max-width:1080px) {
        ul {
            display: none; // float: right;
            // padding-right: 100px;
            >li {
                color: #fff;
                height: 70px;
                width: 110px;
                text-align: center;
                line-height: 70px;
                cursor: pointer;
                &:hover {
                    background: rgba(225, 225, 225, 0.15);
                }
            }
        }
    }
}
</style>


<script type="text/ecmascript-6">
export default {
    data() {
        return {
            navList: [
                { menu: '全网搜索' },
                { menu: '流程定制' },
                { menu: '统计分析' },
                { menu: '投后管理' },
                { menu: '文档管理' },
                { menu: '协同办公' },
                { menu: '风险预警' }
            ]
        }
    },
    methods: {
    }
}
</script>

