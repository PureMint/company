<template>
  <section class="product">
    <v-header></v-header>
    <el-row>
      <el-col :span="24">
        <div class="search">
          <div class="searchBox">
            <div class="searchText"></div>
            <div class="searchImg"></div>
          </div>
        </div>
        </div>
      </el-col>
      <el-col :span="24">
        <div class="custom">
        </div>
      </el-col>
      <el-col :span="24">
        <div class="analyse">
        </div>
      </el-col>
      <el-col :span="24">
        <div class="manage">
        </div>
      </el-col>
      <el-col :span="24">
        <div class="file">
        </div>
      </el-col>
      <el-col :span="24">
        <div class="work">
        </div>
      </el-col>
      <el-col :span="24">
        <div class="alarm">
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
  // margin-top: 70px;
  .search {
    height: 1080px;
    background: url(../../static/img/product/search-bg.png) no-repeat;
    background-size: 100% 100%;
    .searchBox {
      height: 903px;
    }
    .searchText {
      
    }
  }
  .custom {
    height: 1080px;
    background: url(../../static/img/product/custom-bg.png) no-repeat;
    background-size: 100% 100%;
  }
  .analyse {
    height: 1080px;
    background: url(../../static/img/product/analyse-bg.png) no-repeat;
    background-size: 100% 100%;
  }
  .file {
    height: 1080px;
    background: url(../../static/img/product/file-bg.png) no-repeat;
    background-size: 100% 100%;
  }
  .work {
    height: 1080px;
    background: url(../../static/img/product/work-bg.png) no-repeat;
    background-size: 100% 100%;
  }
  .alarm {
    height: 1080px;
    background: url(../../static/img/product/alarm-bg.png) no-repeat;
    background-size: 100% 100%;
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
  },
}
</script>