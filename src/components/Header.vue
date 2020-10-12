<template>
  <div
    :style="{background:background,'border-bottom':noBorder?'none':'1px solid #2a2542'}"
    class="header"
  >
    <span v-if="isBack" @click="$router.go(-1)">
      <i class="iconfont icon-fanhui"></i>
    </span>
    <div class="title">{{name}}</div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: {
    name: {
      type: String,
      default: "去城"
    },
    isBack: {
      type: Boolean,
      default: false
    },
    background: {
      type: String,
      default: "#0e0b1c"
    },
    noBorder: {
      type: Boolean,
      default: false
    }
  }
};
</script>

<style scoped lang="scss">
.header {
  position: fixed;
  background: #0e0b1c;
  top: 0;
  left: 0;
  z-index: 99;
  width: 100%;
  padding: 0.2rem 0.17rem;
  box-sizing: border-box;
  font-size: 0.36rem;
  color: #fff;
  font-weight: 500;
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #2a2542;
  .title {
    flex: 1;
  }
}
</style>
