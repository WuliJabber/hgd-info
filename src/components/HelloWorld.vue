<script setup>
import { ref } from 'vue'
import { Swipe, SwipeItem } from 'vant';
import { showImagePreview } from 'vant';

const show = ref(false)
const handleClick = (item) => {
  console.log(item)
}
const showMoney = () => {
  show.value = true
}
</script>

<template>
  <div class="container">
    <div class="swipe-box">
      <van-swipe :autoplay="3000" lazy-render>
      <van-swipe-item @click="handleClick">
        <img class="img-box" src="../assets/601730098801_.pic.jpg" />
      </van-swipe-item>
      <van-swipe-item>
        <img class="img-box" src="../assets/611730098802_.pic.jpg" />
      </van-swipe-item>
      <van-swipe-item>
        <img class="img-box" src="../assets/621730098803_.pic.jpg" />
      </van-swipe-item>
      <van-swipe-item>
        <img class="img-box" src="../assets/631730098806_.pic.jpg" />
      </van-swipe-item>
      <van-swipe-item>
        <img class="img-box" src="../assets/641730098808_.pic.jpg" />
      </van-swipe-item>
    </van-swipe>
    </div>
    <div class="touxiang">
      <img class="touxiangImg" src="../assets/651730098811_.pic.jpg" alt="">
    </div>
    <div class="info">
      <van-cell-group>
        <van-cell title="姓名" value="刘彤怡" />
        <van-cell title="性别" value="美女" label="是很美的那种美女" />
        <van-cell title="年龄" value="22" />
        <van-cell title="爱好" value="睡觉" />
        <van-cell title="住址" value="湖北武汉" />
        <van-cell title="个性" value="懒" />
      </van-cell-group>
    </div>
    <van-floating-bubble icon="gold-coin-o" @click="showMoney" />
  </div>
  <van-dialog v-model:show="show">
  <img style="height: 360px; width: 360px;margin: 0 auto" src="../assets/WechatIMG66.jpg" />
</van-dialog>
</template>

<style scoped>
.container {
  padding: 16px;
}
.swipe-box {
  height: 200px;
  width: 100%;
}
.img-box {
  height: 200px;
  width: 100%;
}
.touxiang {
  position: relative;
}
.touxiangImg {
  height: 100px;
  width: 100px;
  border-radius: 50px;
  position: absolute;
  top: -50px;
}
.info {
  margin-top: 60px;
}
</style>
