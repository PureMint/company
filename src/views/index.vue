<template>
    <section class="home">
        <div class="banner">
            <el-carousel height="540px">
                <el-carousel-item v-for="item in 4" :key="item">
                    <img src="/static/img/home/banner-1.png" class="img-responsive"></img>
                </el-carousel-item>
            </el-carousel>
        </div>
        <div class="special">
        </div>
    </section>
</template>


<style lang="less" scoped>
.home {
    margin-top: 70px;
    color: black;
    .img-responsive {
        display: inline-block;
        height: 540px;
        max-width: 100%;
    }
    .special {
        height: 707px;
        background: url(../../static/img/home/special-bg.png) no-repeat;
        background-size:100% 100%;
    }
}
</style>


<script>
export default {

}
</script>
