<template>
  <section class="about">
    <v-header></v-header>
    <el-row>
      <el-col :span="24" class="banner">
        <!-- <div @mouseleave="leave($event)" @mouseover="hover($event)"> -->
        <div>
          <div></div>
          <!-- <div :class="{actives: isActive}"> -->
          <div>
            <img src="../../static/img/about/about-us.png" alt="">
            <p style="width:125px;font-size:30px;color:#fff;font-family:'MicrosoftYaHei';padding-bottom:4px;margin-bottom:100px;border-bottom:4px solid #F05E5E;">关于我们</p>
            <p style="width:450px;text-indent:28px;margin:8px;font-size:16px;color:#9aa9ca;line-height:27px" class="animated  fadeInLeft">
              领投者拥有一支技术精湛的专业运维服务队伍，具备陷阱的技术服务水平及丰富的软件系统运维经验。配合服务热线、远程技术支持和先进的服务管理机制
            </p>
          </div>
        </div>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <div class="welcom">{{welcomJ}}</div>
      </el-col>
    </el-row>
    <el-row class="join" :gutter="40">
      <div>
        <el-col class="welImg" :span="5" v-for="(item,index) in welImg" :key="item.index">
          <!-- <div @mouseleave="welLeave(item,index)" @mouseover="welHover(item,index)"> -->
          <div>
            <img :src="item.src" class="img-responsive">
            <div :class="item.welImg_posi"></div>
            <span class="span" v-show="index == 1">我们的休息室</span>
          </div>
        </el-col>
      </div>
    </el-row>
    <el-row>
      <el-col class="fontS" :offset="4" :span="24">
        {{Company}}
      </el-col>
    </el-row>
    <el-row class="gsCompany">
      <el-col :class="{company: index == 0,company1: index == 1,company2: index == 2}" :span="4" v-for="(item,index) in gsCompany" :key="item.index">
        <div>
          <div><img :src="item.src" alt=""></div>
          <div :class="{'color-s': index==1,'color-t': index==2}" style="color:#41578C;font-weight: bold ">{{item.text1}}</div>
          <div style="font-weight: bold;line-height: 20px;font-size: 14px;color: #818693">{{item.text2}}</div>
        </div>
      </el-col>
    </el-row>
    <el-row class="Recruitment">
      <el-col class="fontS" :offset="4" :span="24">
        {{Recruitment}}
      </el-col>
    </el-row>
    <el-row class="tabBotm">
      <el-col :span="6" :offset="4" class="">
        <img src="static/img/about/left.svg" alt="" />
        <img src="static/img/about/right.svg" alt="" />
        <el-tabs v-model="activeName2" type="card" @tab-click="handleClick">
          <el-tab-pane label="财务员" name="first">
            <div class="tabPosi">
              <div v-for="(item,index) in tabContent" :key="item.index">
                <p>{{item.text}}</p>
              </div>
            </div>
          </el-tab-pane>
          <el-tab-pane label="客 服" name="second">
            <div class="tabPosi">
              <div v-for="(item,index) in tabContent" :key="item.index">
                <p>{{item.text}}</p>
              </div>
            </div>
          </el-tab-pane>
          <el-tab-pane label="UI设计" name="third">
            <div class="tabPosi">
              <div v-for="(item,index) in tabContent" :key="item.index">
                <p>{{item.text}}</p>
              </div>
            </div>
          </el-tab-pane>
          <el-tab-pane label="程序员" name="fourth">
            <div class="tabPosi">
              <div v-for="(item,index) in tabContent" :key="item.index">
                <p>{{item.text}}</p>
              </div>
            </div>
          </el-tab-pane>
          <!-- left right btn -->
        </el-tabs>
      </el-col>
      <el-col :span="6" class="ruleForm2">
        <div>
          <el-form label-position="left" :model="ruleForm2" :rules="rules2" ref="ruleForm2" label-width="100px" class="demo-ruleForm">
            <el-form-item label="应聘职位 : " prop="position">
              <el-input v-model="ruleForm2.position" auto-complete="off"></el-input>
            </el-form-item>
            <el-form-item label="姓 名 : " prop="name">
              <el-input v-model="ruleForm2.name" auto-complete="off"></el-input>
            </el-form-item>
            <el-form-item label="电 话 : " prop="phone">
              <el-input v-model="ruleForm2.phone"></el-input>
            </el-form-item>
            <el-form-item label="建 议 : " prop="advise">
              <el-input v-model="ruleForm2.advise"></el-input>
            </el-form-item>
            <el-form-item>
              <el-button type="primary" @click="submitForm('ruleForm2')">提交</el-button>
            </el-form-item>
          </el-form>
        </div>
      </el-col>
    </el-row>
    <v-footer></v-footer>
  </section>
</template>

<style lang="less" scoped>
.about {
  margin-top: 70px;
  overflow: hidden;
  min-width: 1100px;
  .img-responsive {
    display: block;
    height: auto;
    width: 100%;
  }
  .banner {
    position: relative;
    >div>div:nth-child(1) {
      height: 600px;
      background: url(../../static/img/about/about-bg.png) no-repeat;
      background-size: cover;
    }
    >div>div:nth-child(2) {
      position: absolute;
      right: -50%;
      top: 0;
      width: 100%;
      height: 600px;
      transition: all 1s ease;
      background: rgba(76, 84, 104, .7);
      z-index: 0;
      padding: 100px 48px;
      box-sizing: border-box;
      &:hover {
        right: 0;
      }
      img {
        position: absolute;
        top: 98px;
        left: -160px;
      }
    }
    .actives {
      right: 0!important;
    }
  }
}

.welcom {
  width: 100%;
  height: 30px;
  font-size: 30px;
  text-align: center;
  margin: 90px 0 80px 0;
}

.join {
  width: 100%;
  margin-bottom: 86px;
  >div {
    margin: 0 auto;
    >.welImg {
      position: relative;
      .span {
        position: absolute;
        text-align: center;
        top: 37px;
        left: 38%;
      }
      >div {
        overflow: hidden;
        img:hover {
          transition: all 1s ease;
          transform: scale(1.1);
        }
      }
    }
    .welImg_posi1 {
      width: 340px;
      height: 240px;
      position: absolute;
      top: -239px;
      display: none;
      background: rgba(0, 0, 0, 0.5);
    }
    .welImg_posi1_1 {
      width: 340px;
      height: 240px;
      position: absolute;
      top: 0px;
      display: block;
      background: rgba(0, 0, 0, 0.5);
    }
    .welImg_posi2 {
      width: 340px;
      height: 240px;
      position: absolute;
      top: -239px;
      display: none;
      color: black;
      background: rgba(0, 0, 0, 0.5);
      span {
        text-align: center;
        line-height: 200px;
      }
    }
    .welImg_posi2_2 {
      width: 340px;
      height: 240px;
      position: absolute;
      top: 0;
      display: block;
      text-align: center;
      line-height: 200px;
      color: black;
      background: rgba(0, 0, 0, 0.5);
      >span {
        text-align: center;
        line-height: 200px;
      }
    }
    .welImg_posi3 {
      width: 340px;
      height: 240px;
      position: absolute;
      top: -239px;
      display: none;
      background: rgba(0, 0, 0, 0.5);
    }
    .welImg_posi3_3 {
      width: 340px;
      height: 240px;
      position: absolute;
      top: 0;
      display: block;
      background: rgba(0, 0, 0, 0.5);
    }
    >div {
      height: 239px;
    }
    >div:nth-child(1) {
      margin-left: 20%;
    }
  }
}

.fontS {
  font-size: 30px;
}

.gsCompany {
  .company {
    margin-left: 27%;
  }
  .company1 {
    margin-left: 4%;
  }
  .company2 {
    margin-left: 4%;
  }
  >div {
    margin-top: 64px;
    >div {
      >div:nth-child(2) {
        width: 195px;
        font-size: 18px;
        color: #f05e5e;
        margin: 39px 0 0 -40px;
      }
      .color-s {
        color: #41578c;
      }
      .color-t {
        color: #9aa9ca;
      }
      >div:nth-child(3) {
        width: 195px;
        font-size: 14px;
        margin: 25px 0 90px -40px;
        line-height: 20px;
      }
    }
  }
}

.Recruitment {
  margin-bottom: 40px;
}

.ruleForm1 {
  // width: 100%;
  height: 236px;
  padding: 52px 48px;
  background: #f2f4f8;
}

.ruleForm2 {
  margin-left: 20%;
  font-size: 14px;
  >div {
    margin-top: 78px;
    width: 100%;
    height: 236px;
    padding: 52px 48px;
    background: #f2f4f8;
  }
  button {
    float: right;
    background: #f05e5e;
    color: #ffffff;
    border: none;
  }
}

.tabBotm {
  margin-bottom: 90px;
  >div {
    position: relative;
    >img {
      display: inline-block;
      position: absolute;
      top: 0;
      right: 0;
    }
    >img:nth-child(1) {
      margin-right: 20px;
    }
  }
  .elTabs {}
}

.tabPosi {
  margin-top: 18px;
  background: #f2f4f8; // width: 100%;
  height: 236px;
  padding: 52px 48px;
  >div {
    margin: 10px 0;
    p {
      font-size: 14px;
      line-height: 20px;
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
    // var checkAge = (rule, value, callback) => {
    //   if (!value) {
    //     return callback(new Error("年龄不能为空"));
    //   }
    //   setTimeout(() => {
    //     if (!Number.isInteger(value)) {
    //       callback(new Error("请输入数字值"));
    //     } else {
    //       if (value < 18) {
    //         callback(new Error("必须年满18岁"));
    //       } else {
    //         callback();
    //       }
    //     }
    //   }, 1000);
    // };
    // var validatePass = (rule, value, callback) => {
    //   if (value === "") {
    //     callback(new Error("请输入密码"));
    //   } else {
    //     if (this.ruleForm2.checkPass !== "") {
    //       this.$refs.ruleForm2.validateField("checkPass");
    //     }
    //     callback();
    //   }
    // };
    // var validatePass2 = (rule, value, callback) => {
    //   if (value === "") {
    //     callback(new Error("请再次输入密码"));
    //   } else if (value !== this.ruleForm2.pass) {
    //     callback(new Error("两次输入密码不一致!"));
    //   } else {
    //     callback();
    //   }
    // };
    return {
      ruleForm2: {
        position: '',
        name: '',
        phone: '',
        advise: ''
      },
      rules2: {
        position: [{ message: '请输入应聘职位', trigger: 'blur' }],
        name: [{ message: '请输入姓名', trigger: 'blur' }],
        phone: [{ message: '请输入电话', trigger: 'blur' }]
      },
      tabContent: [
        { text: "1、熟练使用Word , Excel等office办公软件" },
        { text: "2、对于网上银行的操作以及银行汇票、本票、支票等票据能够熟练操作" },
        { text: "3、负责编制公司会计凭证，审核、装订及保管各类会计凭证，登记及保管各类账薄" },
        { text: "4、按月编制会计报表，并进行分析汇总，报公司领导备案决策" },
        { text: "5、负责监督公司财务运作情况及时核对现金" }
      ],
      activeName2: "first",
      lounge: true,
      Company: "公司福利",
      Recruitment: "招聘职位",
      welImg_posi1: "welImg_posi1",
      welImg_posi2: "welImg_posi2",
      welImg_posi3: "welImg_posi3",
      welImg_posi1_1: "welImg_posi1_1",
      welImg_posi2_2: "welImg_posi2_2",
      welImg_posi3_3: "welImg_posi3_3",
      isActive: true,
      welcomJ: "欢迎你的加入",
      welImg: [
        {
          src: "./static/img/about/show1.png",
          welImg_posi: "welImg_posi1"
        },
        {
          src: "./static/img/about/show2.png",
          welImg_posi: "welImg_posi2"
        },
        {
          src: "./static/img/about/show3.png",
          welImg_posi: "welImg_posi3"
        }
      ],
      gsCompany: [
        {
          src: "./static/img/about/Company1.png",
          text1: "免费零食 , 等你来拿",
          text2: "公司会员工喜好,定期为员工股购买零食,饮料等各类零食"
        },
        {
          src: "./static/img/about/Company2.png",
          text1: "人性考勤 , 不服来辩",
          text2: "实行电子化考勤,特殊情况申请补卡,按照正常上班记录"
        },
        {
          src: "./static/img/about/Company3.png",
          text1: "扁平管理, 带薪年假",
          text2: "休息日,法定节假日、事假病假、婚假、产假、年休假丧假根据国家政策规定"
        }
      ]
    };
  },
  methods: {
    // submitForm(formName) {
    //   this.$refs[formName].validate(valid => {
    //     if (valid) {
    //       alert("submit!");
    //     } else {
    //       console.log("error submit!!");
    //       return false;
    //     }
    //   });
    // },
    // resetForm(formName) {
    //   this.$refs[formName].resetFields();
    // },
    handleClick() { },
    // hover(e) {
    //   e.preventDefault();
    //   e.stopPropagation();
    //   // alert(0)
    //   this.isActive = true;
    // },
    // leave(e) {
    //   e.preventDefault();
    //   e.stopPropagation();
    //   this.isActive = false;
    // },
    welHover(item, index) {
      console.log(item);
      console.log(index);
      if (index == "0") {
        item.welImg_posi = this.welImg_posi1_1;
      } else if (index == "1") {
        item.welImg_posi = this.welImg_posi2_2;
        this.lounge = true;
      } else {
        item.welImg_posi = this.welImg_posi3_3;
      }
    },
    welLeave(item, index) {
      console.log(item);
      console.log(index);
      if (index == "0") {
        item.welImg_posi = this.welImg_posi1;
      } else if (index == "1") {
        item.welImg_posi = this.welImg_posi2;
      } else {
        item.welImg_posi = this.welImg_posi3;
      }
    },
    goTop() {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    }
  },
  components: {
    vHeader,
    vFooter
  }
};
</script>
