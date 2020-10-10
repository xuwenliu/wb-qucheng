<template>
  <div class="index">
    <Header name="ta的IP" noBorder background="#1F1A37" />
    <div class="top">
      <div class="box"></div>
      <div class="box-real">
        <div class="left">
          <div class="avatar-radius"></div>
        </div>
        <div class="right">
          <div class="right-top">
            <div class="desc">
              <h2>谁还不是个萌萌了</h2>
              <p>去城号：123123124</p>
            </div>
            <div class="attention">
              <span>关注ta</span>
            </div>
          </div>
          <div class="right-tag">
            <ul>
              <li>已实名</li>
              <li>广东广州</li>
              <li>文化传媒</li>
              <li>经纪人</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="card">
        <h2 class="title">
          <span>ta的简介</span>
        </h2>
        <p>
          三六零安全科技股份有限公司（以下简称 “360公司”是中国最大的互联网和安全服务提供商。公司创立于2005
          年，是互联网免费安全的首倡者，先后推出360安全士360手机卫士、360安全浏览器等国民级安全产品PC安全产品月活用户达5亿，移动安全产品月活超4.6亿。中最大的互联网和安全服务提供中国最大的互联网和安全服务提供中国最大的互联网和安全服务提供中国最大的互联网和安全服务提供中国最大的互联网和安全服务提供共安全服务提供中国最安全服务提供中国最安全服务提安全服务
        </p>
      </div>
    </div>

    <div class="photo-list">
      <ul class="clearfix">
        <li>
          <img src="../assets/img/img3.png" alt />
        </li>
        <li>
          <img src="../assets/img/img3.png" alt />
        </li>
        <li>
          <img src="../assets/img/img3.png" alt />
        </li>
        <li>
          <img src="../assets/img/img3.png" alt />
        </li>
        <li>
          <img src="../assets/img/img3.png" alt />
        </li>
        <li>
          <img src="../assets/img/img3.png" alt />
        </li>
      </ul>
    </div>
    <div class="card card-business">
      <h2 class="title">
        <span>ta的业务</span>
      </h2>
      <p>三六零安全科技股份有限公司（以下简称 “360公司”是中国最大的互联网和安全服务提供商。公司创立于2005</p>
      <p>三六零安全科技股份有限公司（以下简称 “360公司”是中国最大的互联网和安全服务提供商。公司创立于2005</p>
      <p>三六零安全科技股份有限公司（以下简称 “360公司”是中国最大的互联网和安全服务提供商。公司创立于2005</p>
      <p>三六零安全科技股份有限公司（以下简称 “360公司”是中国最大的互联网和安全服务提供商。公司创立于2005</p>
    </div>
    <div class="love-box">
      <img class="love-icon" src="../assets/img/love_icon.png" alt />
      <div class="love">
        <img src="../assets/img/love.png" alt />
        <span>可爱</span>
      </div>
      <div class="love">
        <img src="../assets/img/love.png" alt />
        <span>有爱</span>
      </div>
      <div class="love">
        <img src="../assets/img/love.png" alt />
        <span>萌萌哒</span>
      </div>
      <div class="love">
        <img src="../assets/img/love.png" alt />
        <span>超级温柔</span>
      </div>
      <div class="love">
        <img src="../assets/img/love.png" alt />
        <span>热情</span>
      </div>
    </div>

    <Footer :current-index="1"></Footer>
  </div>
</template>

<script>
import Header from "@/components/Header";
import Footer from "@/components/Footer";
export default {
  name: "Home",
  components: {
    Header,
    Footer
  }
};
</script>

<style scoped lang="scss">
.index {
  background: #0e0b1c;
  padding-bottom: 1.2rem;
  padding-top: 0.7rem;
}
.top {
  overflow: hidden;
  position: relative;
}
.box {
  width: 150%;
  height: 7.28rem;
  background: #1f1a37;
  border-radius: 50%;
  margin-left: -20%;
  margin-top: -50%;
}
.box-real {
  position: absolute;
  z-index: 1;
  top: 0;
  width: 100%;
  padding: 0.2rem 0.28rem;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .left {
    .avatar-radius {
      width: 0.88rem;
      height: 0.88rem;
      background: url("../assets/img/avatar_radius.png") no-repeat;
      background-size: contain;
    }
  }
  .right {
    flex: 1;
    padding-left: 0.2rem;
    .right-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      .desc {
        h2 {
          font-size: 0.27rem;
          font-weight: 600;
          color: #ffffff;
        }
        p {
          font-size: 0.16rem;
          font-weight: 400;
          color: #ffffff;
        }
      }
      .attention {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-right: 0.2rem;
        font-size: 0.19rem;
        font-weight: 500;
        color: #ffffff;
        padding: 0 0.12rem;
        height: 0.48rem;
        background: linear-gradient(180deg, #f885a3 0%, #ee4e6a 100%);
        border-radius: 0.16rem;
      }
    }
    .right-tag {
      margin-top: 0.2rem;
      ul {
        font-size: 0.16rem;
        text-align: left;
        li {
          font-size: 0.16rem;
          font-weight: 400;
          color: #ff4b82;
          border: 1px solid #ff4b82;
          border-radius: 0.14rem;
          display: inline-block;
          margin-right: 0.11rem;
          padding: 0 0.11rem;
        }
      }
    }
  }
}
.card {
  background: #2d2941;
  box-shadow: 0rem 0rem 0.08rem 0rem rgba(0, 0, 0, 0.37);
  border-radius: 0.13rem;
  margin: 0 0.4rem;
  margin-top: -22%;
  .title {
    font-size: 0.19rem;
    font-weight: 600;
    color: #ff4b82;
    padding: 0.05rem 0;
    border-bottom: 1px dashed #fff;
    margin: 0 0.1rem;
    span {
      position: relative;
      &::after,
      &::before {
        content: "";
        width: 0.36rem;
        height: 0.03rem;
        background: #ff4b82;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        right: -0.51rem;
      }
      &::before {
        right: auto;
        left: -0.51rem;
      }
    }
  }
  p {
    font-size: 0.16rem;
    font-weight: 400;
    color: #ffffff;
    padding: 0.1rem;
    text-align: left;
  }
}
.photo-list {
  padding: 0 0.32rem;
  margin-top: 0.16rem;
  ul {
    li {
      float: left;
      width: 31%;
      margin-left: 0.14rem;
      margin-top: 0.14rem;
      img {
        width: 100%;
        height: 100%;
        display: block;
      }
    }
  }
}
.card-business {
  margin-top: 0.16rem;
  p {
    &::before {
      content: "1";
      width: 0.24rem;
      height: 0.24rem;
      background: #ff4b82;
      border-radius: 50%;
      display: inline-block;
      text-align: center;
      line-height: 0.24rem;
      margin-right: 0.12rem;
    }
    &:nth-of-type(2) {
      &::before {
        content: "2";
      }
    }
    &:nth-of-type(3) {
      &::before {
        content: "3";
      }
    }
    &:nth-of-type(4) {
      &::before {
        content: "4";
      }
    }
  }
}
.love-box {
  margin: 0.43rem 0.32rem;
  height: 2rem;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  .love-icon {
    width: 1.13rem;
    height: 1.13rem;
    vertical-align: middle;
  }
  .love {
    font-size: 0.16rem;
    display: inline-block;
    position: absolute;
    left: 0;
    top: 0;
    animation: heartBeat 1s infinite;
    img {
      width: 0.41rem;
      height: 0.41rem;
    }
    span {
      font-size: 0.16rem;
      font-weight: 500;
      color: #ffffff;
    }
    &:nth-child(3) {
      right: 0.5rem;
      left: auto;
      top: 0;
      animation: heartBeat 1.5s infinite;
    }
    &:nth-child(4) {
      left: 1rem;
      top: auto;
      bottom: 0;
      animation: heartBeat 2s infinite;
    }
    &:nth-child(5) {
      right: 0.3rem;
      left: auto;
      bottom: 0;
      top: auto;
      animation: heartBeat 2.5s infinite;
    }
    &:nth-child(6) {
      left: 50%;
      bottom: 0;
      top: auto;
      animation: heartBeat 3s infinite;
    }
  }
}

@-webkit-keyframes heartBeat {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }

  14% {
    -webkit-transform: scale(1.3);
    transform: scale(1.3);
  }

  28% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }

  42% {
    -webkit-transform: scale(1.3);
    transform: scale(1.3);
  }

  70% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

@keyframes heartBeat {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }

  14% {
    -webkit-transform: scale(1.3);
    transform: scale(1.3);
  }

  28% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }

  42% {
    -webkit-transform: scale(1.3);
    transform: scale(1.3);
  }

  70% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}
</style>
