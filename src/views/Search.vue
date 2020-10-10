<template>
  <div class="index">
    <Header isBack name="去城" />
    <div class="title">
      <h2>
        <span>请选择您要搜索的行业</span>
        <div class="line"></div>
      </h2>
    </div>
    <div class="service">
      <img src="../assets/img/service.png" alt />
      <span>总计0人</span>
    </div>
    <div class="list">
      <ul class="clearfix">
        <li
          @click="choose(index)"
          v-for="(item,index) in list"
          :key="item.name"
          :class="index === chooseIndex ?'active':''"
        >
          <div class="bg">
            <img :src="item.icon" alt />
            <h2>{{item.name}}</h2>
            <span>总计{{item.total}}人</span>
          </div>
          <div class="line"></div>
        </li>
      </ul>
    </div>
    <div class="btn">
      <div @click="$router.go(-1)" class="back">返回</div>
      <div class="ok">确定</div>
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header";
export default {
  name: "Search",
  data() {
    return {
      chooseIndex: "",
      list: [
        {
          icon: require("../assets/img/icon1.png"),
          name: "文化传媒",
          total: 0
        },
        {
          icon: require("../assets/img/icon2.png"),
          name: "教育培训",
          total: 0
        },
        { icon: require("../assets/img/icon3.png"), name: "金融", total: 0 },
        {
          icon: require("../assets/img/icon4.png"),
          name: "传统制造",
          total: 0
        },
        {
          icon: require("../assets/img/icon5.png"),
          name: "医疗保健",
          total: 0
        },
        {
          icon: require("../assets/img/icon6.png"),
          name: "法律服务",
          total: 0
        },
        {
          icon: require("../assets/img/icon7.png"),
          name: "事业单位",
          total: 0
        },
        { icon: require("../assets/img/icon8.png"), name: "IT软件", total: 0 },
        { icon: require("../assets/img/icon9.png"), name: "学生", total: 0 },
        {
          icon: require("../assets/img/icon10.png"),
          name: "其他行业",
          total: 0
        }
      ]
    };
  },
  components: {
    Header
  },
  methods: {
    choose(index) {
      this.chooseIndex = index;
    }
  }
};
</script>

<style scoped lang="scss">
.index {
  background: #0e0b1c;
  padding-top: 1rem;
  padding-bottom: 1.65rem;
}
.title {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0.23rem 0;
  h2 {
    font-size: 0.28rem;
    font-weight: 600;
    color: #ffffff;
    position: relative;
    display: inline-block;
    .line {
      height: 0.08rem;
      background: #ff4b82;
      border-radius: 0.11rem;
    }

    &::before,
    &::after {
      content: "";
      width: 0.08rem;
      height: 0.08rem;
      display: block;
      position: absolute;
      left: -0.2rem;
      top: 50%;
      transform: translateY(-50%);
      background: #ff4b82;
    }
    &::after {
      right: -0.2rem;
      left: auto;
    }
  }
}
.service {
  background: #fff8f8;
  border-radius: 0.13rem;
  margin: 0 0.2rem;
  padding: 0.15rem 0;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  img {
    width: 0.96rem;
    height: 0.93rem;
    vertical-align: middle;
  }

  span {
    font-size: 0.19rem;
    font-weight: 400;
    color: #e04141;
  }
}
.list {
  padding: 0 0.27rem;
  ul {
    li {
      width: 50%;
      float: left;
      margin-top: 0.26rem;
      .line {
        width: 84%;
        height: 0.06rem;
        background: #eb95ff;
        margin: 0.05rem auto 0;
      }
      .bg {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        padding: 0.06rem 0;
        background: url("../assets/img/sanjiao.png") center center no-repeat;
        background-size: 90% 100%;
        img {
          width: 0.51rem;
          height: 0.51rem;
          display: block;
        }
        h2 {
          font-size: 0.3rem;
          font-weight: 600;
          color: #a97fff;
          margin: 0.05rem 0;
        }
        span {
          font-size: 0.19rem;
          font-weight: 400;
          color: #bd5aef;
        }
      }
      &.active {
        .line {
          background: #e04141 !important;
        }
        h2 {
          color: #ff7f7f !important;
        }
        span {
          color: #e04141 !important;
        }
      }
      &:nth-child(2) {
        .line {
          background: #41dc66;
        }
        h2 {
          color: #15ad36;
        }
        span {
          color: #5fc221;
        }
      }
      &:nth-child(3) {
        .line {
          background: #ffec4b;
        }
        h2 {
          color: #ffec4b;
        }
        span {
          color: #ffec4b;
        }
      }
      &:nth-child(4) {
        .line {
          background: #ff814b;
        }
        h2 {
          color: #ff7e4b;
        }
        span {
          color: #ff9b4b;
        }
      }
      &:nth-child(5) {
        .line {
          background: #14c16d;
        }
        h2 {
          color: #28f17d;
        }
        span {
          color: #20df77;
        }
      }
      &:nth-child(6) {
        .line {
          background: #d04472;
        }
        h2 {
          color: #ff4b70;
        }
        span {
          color: #ff4b79;
        }
      }
      &:nth-child(7) {
        .line {
          background: #c17e18;
        }
        h2 {
          color: #e9950d;
        }
        span {
          color: #e4950d;
        }
      }

      &:nth-child(8) {
        .line {
          background: #4b7aff;
        }
        h2 {
          color: #4b80ff;
        }
        span {
          color: #4ba1ff;
        }
      }
      &:nth-child(9) {
        .line {
          background: #fc3ba9;
        }
        h2 {
          color: #fc37a1;
        }
        span {
          color: #fd3eae;
        }
      }
      &:nth-child(10) {
        .line {
          background: #9c5ff9;
        }
        h2 {
          color: #9c5ef9;
        }
        span {
          color: #fd4cf2;
        }
      }
    }
  }
}
.btn {
  position: fixed;
  bottom: 0;
  width: 100%;
  box-sizing: border-box;
  padding: 0.35rem 0.5rem;
  display: flex;
  justify-content: center;
  background: #0e0b1c;
  .back,
  .ok {
    width: 1.92rem;
    line-height: 0.6rem;
    text-align: center;
    color: #fff;
    font-size: 0.29rem;
    font-weight: 600;
    border-radius: 0.3rem;
    background: url("../assets/img/back.png") center center no-repeat;
    background-size: cover;
  }
  .ok {
    margin-left: 0.22rem;
    background: url("../assets/img/ok.png") center center no-repeat;
  }
}
</style>
