<template>
  <div class="index">
    <!-- <Header /> -->
    <div class="search">
      <input class="input" type="text" placeholder="输入去城号/手机号/名字找ta" />
      <button class="btn">搜索</button>
    </div>
    <div class="nav">
      <ul>
        <li @click="navChange(0)" :class="nav===0?'active':''">个人</li>
        <li @click="navChange(1)" :class="nav===1?'active':''">
          商家
          <span v-if="nav===1" class="ad-group">广告联盟</span>
        </li>
      </ul>
      <div v-if="nav===0" class="more" @click="goSearch">
        <img src="../assets/img/hot.png" alt />
        <span>
          选择行业
          <i class="iconfont icon-gengduo"></i>
        </span>
      </div>
      <div v-if="nav===1" class="address">
        <span class="position">
          <img src="../assets/img/position.png" alt />杭州
        </span>
        <span class="all">全国</span>
      </div>
    </div>
    <div v-if="nav===0">
      <div class="card">
        <div class="card-top">
          <div class="bg1">
            <div class="left">
              <img src="../assets/img/avatar.png" alt class="avatar" />
              <h2>+关注</h2>
              <span>35分钟前</span>
            </div>
            <div class="right">
              <div class="title">
                <h2>转角的爱在上海</h2>
                <ul class="tag">
                  <li>**伦</li>
                  <li>广东广州</li>
                  <li>文化传媒</li>
                  <li>经纪人</li>
                </ul>
              </div>
              <div class="desc">简介：毕业于北京舞蹈学院，从教年限：13年，原中国国儿童艺术剧院演员，温州市鹿城舞蹈家协会会员并温州市鹿城舞蹈家协会会员并</div>
            </div>
          </div>
          <div class="bg2">
            <span>ta的业务：广告代言；电视剧拍摄；明星小视频</span>
          </div>
        </div>
        <div class="card-photo">
          <img src="../assets/img/img1.png" alt />
          <img src="../assets/img/img2.png" alt />
          <img src="../assets/img/img3.png" alt />
        </div>
      </div>
      <div class="card">
        <div class="card-top">
          <div class="bg1">
            <div class="left">
              <img src="../assets/img/avatar.png" alt class="avatar" />
              <span class="attention">已关注</span>
              <span>35分钟前</span>
            </div>
            <div class="right">
              <div class="title">
                <h2>转角的爱在上海</h2>
                <ul class="tag">
                  <li>**伦</li>
                  <li>广东广州</li>
                  <li>文化传媒</li>
                  <li>经纪人</li>
                </ul>
              </div>
              <div class="desc">简介：毕业于北京舞蹈学院，从教年限：13年，原中国国儿童艺术剧院演员，温州市鹿城舞蹈家协会会员并温州市鹿城舞蹈家协会会员并</div>
            </div>
          </div>
          <div class="bg2">
            <span>ta的业务：广告代言；电视剧拍摄；明星小视频</span>
          </div>
        </div>
        <div class="card-photo">
          <img src="../assets/img/img1.png" alt />
          <img src="../assets/img/img2.png" alt />
          <img src="../assets/img/img3.png" alt />
        </div>
      </div>
      <div class="create-ip">
        <img src="../assets/img/ip.png" alt />
      </div>
    </div>

    <div class="merchant" v-if="nav===1">
      <div class="fast">
        <ul>
          <li
            :class="fastIndex === index ? 'active':''"
            v-for="(item,index) in fastList"
            :key="item.name"
            @click="fastChange(index)"
          >
            <img :src="item.icon" alt />
            <span>{{item.name}}</span>
          </li>
        </ul>
      </div>

      <div class="choose-title">
        <p @click="openDailog">
          <span>选</span> 择细分类别
        </p>
      </div>

      <div class="card">
        <div class="card-top">
          <div class="bg1">
            <div class="left">
              <img src="../assets/img/avatar.png" alt class="avatar" />
            </div>
            <div class="right">
              <div class="title">
                <h2>
                  杭州滨江长河明镜眼镜店
                  <span>
                    100元
                    <img src="../assets/img/jbbf.png" alt />
                  </span>
                </h2>
              </div>
              <div class="address-limit">
                <p>
                  <img src="../assets/img/bzbf.png" alt />
                  <span>杭州市 星光大道广场</span>
                </p>
                <p>已分80元</p>
              </div>
            </div>
          </div>
          <div class="bg2">
            <span>新客户配眼镜全场8折送镜框限本周</span>
          </div>
        </div>
        <div class="card-bottom">
          <div class="box">
            <span>+关注</span>
            <div class="right">
              <p>
                <span>点击进入</span>
                <img src="../assets/img/right-finger.png" alt />
              </p>
              <button>
                <img src="../assets/img/axbf.png" alt />
                <span>1000人</span>
              </button>
            </div>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-top">
          <div class="bg1">
            <div class="left">
              <img src="../assets/img/avatar.png" alt class="avatar" />
            </div>
            <div class="right">
              <div class="title">
                <h2>
                  杭州滨江长河明镜眼镜店
                  <span>
                    100元
                    <img src="../assets/img/jbbf.png" alt />
                  </span>
                </h2>
              </div>
              <div class="address-limit">
                <p>
                  <img src="../assets/img/gsbf.png" alt />
                  <span>文化传媒 报社</span>
                </p>
                <p>已分80元</p>
              </div>
            </div>
          </div>
          <div class="bg2">
            <span>新客户配眼镜全场8折送镜框限本周</span>
          </div>
        </div>
        <div class="card-bottom">
          <div class="box">
            <span>+关注</span>
            <div class="right">
              <p>
                <span>点击进入</span>
                <img src="../assets/img/right-finger.png" alt />
              </p>
              <button>
                <img src="../assets/img/axbf.png" alt />
                <span>1000人</span>
              </button>
            </div>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-top">
          <div class="bg1">
            <div class="left">
              <img src="../assets/img/avatar.png" alt class="avatar" />
            </div>
            <div class="right">
              <div class="title">
                <h2>
                  杭州滨江长河明镜眼镜店
                  <span>
                    100元
                    <img src="../assets/img/jbbf.png" alt />
                  </span>
                </h2>
              </div>
              <div class="address-limit">
                <p>
                  <img src="../assets/img/gsbf.png" alt />
                  <span>文化传媒 报社</span>
                </p>
                <p>已分80元</p>
              </div>
            </div>
          </div>
          <div class="bg2">
            <span>新客户配眼镜全场8折送镜框限本周</span>
          </div>
        </div>
        <div class="card-bottom">
          <div class="box">
            <span>+关注</span>
            <div class="right">
              <p>
                <span>点击进入</span>
                <img src="../assets/img/right-finger.png" alt />
              </p>
              <button>
                <img src="../assets/img/axbf.png" alt />
                <span>1000人</span>
              </button>
            </div>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-top">
          <div class="bg1">
            <div class="left">
              <img src="../assets/img/avatar.png" alt class="avatar" />
            </div>
            <div class="right">
              <div class="title">
                <h2>
                  杭州滨江长河明镜眼镜店
                  <span>
                    100元
                    <img src="../assets/img/jbbf.png" alt />
                  </span>
                </h2>
              </div>
              <div class="address-limit">
                <p>
                  <img src="../assets/img/gsbf.png" alt />
                  <span>文化传媒 报社</span>
                </p>
                <p>已分80元</p>
              </div>
            </div>
          </div>
          <div class="bg2">
            <span>新客户配眼镜全场8折送镜框限本周</span>
          </div>
        </div>
        <div class="card-bottom">
          <div class="box">
            <span>+关注</span>
            <div class="right">
              <p>
                <span>点击进入</span>
                <img src="../assets/img/right-finger.png" alt />
              </p>
              <button>
                <img src="../assets/img/axbf.png" alt />
                <span>1000人</span>
              </button>
            </div>
          </div>
        </div>
      </div>

      <div class="create-ip">
        <img src="../assets/img/adbf.png" alt />
      </div>

      <div v-if="showDailog" @click="closeDailog" class="dailog">
        <div class="dailog-body clearfix">
          <div class="content">
            <ul class="clearfix">
              <li
                v-for="(item,index) in category"
                :key="item"
                @click="chooseCategory(index)"
                :class="categoryIndex === index ? 'active':''"
              >
                <span>{{item}}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <Footer></Footer>
  </div>
</template>

<script>
// import Header from "@/components/Header";
import Footer from "@/components/Footer";
export default {
  name: "Home",
  components: {
    // Header,
    Footer
  },
  data() {
    return {
      nav: 0,
      fastIndex: 0,
      showDailog: false,
      categoryIndex: "",
      category: [
        "KTV",
        "酒吧",
        "茶馆",
        "轰趴团建",
        "电影演出",
        "电玩密室",
        "其他"
      ],
      fastList: [
        {
          name: "美食/生活购物",
          icon: require("../assets/img/msbf.png")
        },
        {
          name: "酒店/旅游",
          icon: require("../assets/img/jdbf.png")
        },
        {
          name: "娱乐",
          icon: require("../assets/img/ylbf.png")
        },
        {
          name: "生活",
          icon: require("../assets/img/shfwbf.png")
        },
        {
          name: "服务类",
          icon: require("../assets/img/fwbf.png")
        },
        {
          name: "其他",
          icon: require("../assets/img/qtbf.png")
        }
      ]
    };
  },
  methods: {
    goSearch() {
      this.$router.push({
        name: "Search"
      });
    },
    navChange(nav) {
      this.nav = nav;
    },
    fastChange(index) {
      this.fastIndex = index;
    },
    openDailog() {
      this.showDailog = true;
    },
    closeDailog() {
      this.showDailog = false;
    },
    chooseCategory(index) {
      this.categoryIndex = index;
      this.closeDailog();
    }
  },
  watch: {
    showDailog(val) {
      if (val) {
        document.body.style.position = "fixed";
      } else {
        document.body.style.position = "static";
      }
    }
  }
};
</script>

<style scoped lang="scss">
.index {
  background: #0e0b1c;
  // padding-top: 1rem;
  padding-bottom: 1.2rem;
}

.search {
  padding: 0.18666rem 0.4rem;
  height: 0.5rem;
  display: flex;
  .btn {
    width: 0.9rem;
    background: #ff4b82;
    color: #fff;
    border: none;
    outline: none;
    border-radius: 0 0.32rem 0.32rem 0;
    font-size: 0.19rem;
    font-weight: 500;
  }
  .input {
    flex: 1;
    border-radius: 0.32rem 0 0 0.32rem;
    border: none;
    padding-left: 0.26667rem;
    outline: none;
    font-size: 0.2rem;
  }
}
.nav {
  padding: 0.1866rem 0 0.25rem;
  margin: 0 0.26667rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #979797;
  ul {
    display: flex;
    li {
      font-weight: 500;
      color: #ffffff;
      font-size: 0.24rem;
      line-height: 0.32rem;
      margin-right: 0.4rem;
      position: relative;
      .ad-group {
        position: absolute;
        font-size: 0.16rem;
        display: block;
        bottom: -0.24rem;
        width: 200%;
        right: -200%;
      }
      &.active {
        color: #ff4b82;
        font-size: 0.32rem;
        position: relative;
        &::after {
          content: "";
          position: absolute;
          width: 100%;
          height: 0.05rem;
          background: #ff4b82;
          display: block;
          bottom: -0.15rem;
        }
      }
    }
  }
  .more {
    display: flex;
    img {
      width: 0.21rem;
      height: 0.24rem;
      vertical-align: middle;
      margin-right: 0.1rem;
    }
    span {
      font-weight: 600;
      color: #ffffff;
      line-height: 0.27rem;
      font-size: 0.19rem;
      i {
        vertical-align: bottom;
      }
    }
  }
  .address {
    font-size: 0.21rem;
    .position {
      img {
        width: 0.16rem;
        height: 0.31rem;
      }
      font-size: 0.21rem;
      font-weight: 600;
      color: #fd2e2e;
      margin-right: 0.2rem;
    }
    .all {
      font-size: 0.21rem;
      font-weight: 600;
      color: #ffffff;
    }
  }
}
.card {
  padding: 0.04rem 0;
  .card-top {
    position: relative;
    min-height: 2rem;

    .bg1 {
      position: absolute;
      z-index: 1;
      background: url(../assets/img/bg1.png) center center no-repeat;
      background-size: 100% 100%;
      display: flex;
      padding: 0.2rem;
      margin: 0 0.08rem;
      box-sizing: border-box;
      .left {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        margin-right: 0.05rem;
        .avatar {
          width: 0.7rem;
          height: 0.7rem;
          display: block;
          align-self: flex-start;
        }
        h2 {
          font-size: 0.16rem;
          font-weight: 500;
          color: #ff4b82;
          align-self: flex-start;
          margin: 0.04rem 0;
        }
        span {
          font-weight: 500;
          color: #999999;
          font-size: 0.11rem;
          &.attention {
            margin: 0.04rem 0;
          }
        }
      }
      .right {
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        .title {
          text-align: left;
          font-size: 0.32rem;
          h2 {
            display: inline;
            font-size: 0.19rem;
            font-weight: 500;
            color: #fffdfe;
            span {
              float: right;
              font-size: 0.19rem;
              font-weight: 500;
              color: #ffe94b;
              img {
                width: 0.61333rem;
                vertical-align: middle;
                margin-left: 0.1rem;
              }
            }
          }
        }
        .tag {
          display: inline;
          li {
            padding: 0 0.05rem;
            font-size: 0.13rem;
            font-weight: 400;
            color: #ff4b82;
            border-radius: 0.14rem;
            border: 1px solid #ff4b82;
            text-align: center;
            display: inline-block;
            margin-left: 0.1rem;
          }
        }
        .desc {
          font-size: 0.16rem;
          font-weight: 400;
          color: #fffdfe;
          text-align: left;
          overflow: hidden;
          text-overflow: ellipsis;
          display: -webkit-box;
          -webkit-box-orient: vertical;
          -webkit-line-clamp: 2;
        }
        .address-limit {
          display: flex;
          justify-content: space-between;
          align-items: center;
          margin-bottom: 0.1rem;
          p {
            font-size: 0.19rem;
            font-weight: 500;
            color: #bfba92;
            img {
              width: 0.29rem;
              height: 0.27rem;
              vertical-align: middle;
              margin-right: 0.05rem;
            }
            span {
              font-size: 0.19rem;
              font-weight: 400;
              color: #fffdfe;
            }
          }
        }
      }
    }
    .bg2 {
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      z-index: 0;
      bottom: -0.2rem;
      height: 0.9rem;
      width: 86%;
      background: url(../assets/img/bg2.png) center center no-repeat;
      background-size: 100% 100%;
      span {
        display: block;
        font-size: 0.16rem;
        font-weight: 400;
        color: #833838;
        line-height: 0.53333rem;
        position: absolute;
        bottom: 0;
        left: 50%;
        width: 100%;
        transform: translateX(-50%);
      }
    }
  }
  .card-bottom {
    padding: 0 0 0.2rem;
    margin: 0 0.23rem;
    border-bottom: 1px solid #979797;

    .box {
      display: flex;
      justify-content: space-between;
      align-items: center;
      span {
        font-size: 0.19rem;
        font-weight: 500;
        color: #ff4b82;
      }
      .right {
        display: flex;
        align-items: center;
        p {
          font-size: 0.16rem;
          margin-right: 0.07rem;
          span {
            font-size: 0.16rem;
            font-weight: 500;
            color: #f8f8f4;
          }
          img {
            width: 0.42rem;
            height: 0.27rem;
            vertical-align: middle;
            margin-left: 0.06rem;
          }
        }
        button {
          background: url("../assets/img/btn-bg.png") center center no-repeat;
          background-size: cover;
          border: none;
          padding: 0.03rem 0.12rem;
          outline: none;
          img {
            width: 0.36rem;
            height: 0.31rem;
          }
          span {
            font-size: 0.19rem;
            font-weight: 500;
            color: #b04100;
          }
        }
      }
    }
  }

  .card-photo {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.3rem 0 0.07rem;
    margin: 0 0.23rem;
    border-bottom: 1px solid #979797;

    img {
      width: 32%;
      vertical-align: middle;
      border-radius: 0.1rem;
    }
  }
}
.create-ip {
  position: fixed;
  right: 0.452rem;
  bottom: 2rem;
  z-index: 99;
  img {
    width: 1.67rem;
    height: 0.64rem;
    display: block;
  }
}
.merchant {
  .card {
    .card-top {
      .bg1 {
        width: 97%;
      }
      .bg2 {
        bottom: 0.3rem;
      }
    }
  }
  .fast {
    ul {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      padding: 0 0.15rem;
      li {
        margin-top: 0.2rem;
        padding: 0.07rem 0;
        width: 31%;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 0.46rem;
        background: #151822;
        box-shadow: 0rem 0rem 0.03rem 0rem rgba(141, 141, 141, 0.5);
        border-radius: 0.06rem;
        &.active {
          background: #fff;
        }
        &:nth-child(2) {
          span {
            color: #e34adf;
          }
        }
        &:nth-child(3) {
          span {
            color: #fa7f7f;
          }
        }
        &:nth-child(4) {
          span {
            color: #7994c9;
          }
        }
        &:nth-child(5) {
          span {
            color: #fa1e1e;
          }
        }
        &:nth-child(6) {
          span {
            color: #3b48e0;
          }
        }
        img {
          width: 0.3rem;
          height: 0.3rem;
          vertical-align: middle;
          margin-right: 0.14rem;
        }
        span {
          font-size: 0.24rem;
          font-weight: 500;
          color: #f97c1c;
        }
      }
    }
  }
  .choose-title {
    text-align: right;
    font-size: 0.22rem;
    font-weight: 500;
    color: #e3b5bb;
    margin: 0.1rem 0.23rem;
    padding: 0.1rem;
    border-bottom: 1px solid #979797;

    p {
      display: inline-block;
      span {
        width: 0.33rem;
        height: 0.33rem;
        display: inline-block;
        color: #fffdfe;
        background: #936b6b;
        border-radius: 0.05rem;
        text-align: center;
      }
    }
  }
}
.dailog {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
  width: 100%;
  z-index: 100;
  .dailog-body {
    padding: 0 0.14rem;
    margin-top: 3.8rem;

    .content {
      float: right;
      background: #ffecdf;
      box-shadow: 0 2px 4px 0 #000000;
      border-radius: 0 0 0.14rem 0.14rem;
      max-width: 5.3rem;
      padding-bottom: 0.17rem;
      margin-top: 0.1rem;
      ul {
        li {
          width: 1.26rem;
          margin-top: 0.24rem;
          float: left;
          padding: 0 0.2rem;
          border-left: 0.02rem solid #979797;
          font-size: 0.22rem;
          font-weight: 400;
          color: #333333;
          &:nth-child(3n-2) {
            border: none;
          }
          &.active {
            span {
              background: #ff4b82;
              color: #f9f9f9;
              padding: 0.06rem 0.1rem;
              border-radius: 0.08rem;
            }
          }
        }
      }
    }
  }
}
</style>
