<template>
  <div class="footer">
    <ul>
      <router-link tag="li" :to="{name:'Home'}" :class="currentIndex===0?'active':''">
        <img src="http://placehold.it/218x218" alt />
        <span>去城</span>
      </router-link>
      <router-link tag="li" :to="{name:'Mine'}" :class="currentIndex===1?'active':''">
        <img src="http://placehold.it/218x218" alt />
        <span>ta</span>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: {
    currentIndex: {
      type: Number,
      default: 0
    }
  }
};
</script>

<style scoped lang="scss">
.footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background: #0e0b1c;
  z-index: 100;
  ul {
    height: 1.2rem;
    display: flex;
    align-items: center;
    li {
      flex: 1;
      font-size: 0.16rem;
      color: #fff;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      &.active {
        color: #ff4b82;
      }
      span{
        font-size: 0.24rem;
      }
      img {
        width: 0.56rem;
        height: 0.56rem;
        display: block;
      }
    }
  }
}
</style>
