<script setup lang="ts">
import { onMounted, ref } from "vue";

const learn = ref();
const underLine = ref();
onMounted(()=>{
  underLine.value=window.getComputedStyle(learn.value).width;
})
</script>

<template>
  <div class="home-main">
    <div class="home-header"></div>
    <div class="header-row">
      <div class="row-text">
        <div class="text-area left-text">
          <div class="text-title">Transform your<br/>brand</div>
          <div class="text-content">This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.</div>
          <div class="text-learn" ref="learn">LEARN MORE</div>
          <div class="text-underline left-learn"></div>
        </div>
      </div>
      <div class="home-transform"></div>
    </div>
    <div class="header-row">
      <div class="home-stand-out"></div>
      <div class="row-text">
        <div class="text-area right-text">
          <div class="text-title">Stand out to the right<br/>audience</div>
          <div class="text-content">This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.This is a test.</div>
          <div class="text-learn">LEARN MORE</div>
          <div class="text-underline right-learn"></div>
        </div>
      </div>
    </div>
    <div class="header-row">
      <div class="home-graphic-design"></div>
      <div class="home-photography"></div>
    </div>
  </div>
</template>

<style scoped>
.home-main {
  width: 100%;
}

.home-header {
  background-image: url(/images/desktop/image-header.jpg);
  width: 100%;
  height: 800px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
  background-color: #3ebfff;
}

.header-row {
  display: flex;
  align-items: center;
  justify-content: center;
}

.header-row > div {
  width: 50%;
  height: 600px;
}

.row-text {
  background-color: #fffbf8;
}

.home-transform {
  background-image: url(/images/desktop/image-transform.jpg);
  background-repeat: no-repeat;
  background-position: left;
  background-size: contain;
  background-color: #ffd600;
}

.home-stand-out {
  background-image: url(/images/desktop/image-stand-out.jpg);
  background-repeat: no-repeat;
  background-position: right;
  background-size: contain;
  background-color: #fe7f6e;
}

.home-graphic-design {
  background-image: url(/images/desktop/image-graphic-design.jpg);
  background-repeat: no-repeat;
  background-position: right;
  background-size: contain;
  background-color: #9fdccd;
}

.home-photography {
  background-image: url(/images/desktop/image-photography.jpg);
  background-repeat: no-repeat;
  background-position: left;
  background-size: contain;
  background-color: #5dd2fe;
}

.text-area {
  height: 100%;
  width: 600px;
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: center;
}

.left-text {
  margin-left: auto;
  padding-left: 100px;
}

.right-text {
  margin-right: auto;
  padding-left: 100px;
}

.text-title {
  font-weight: 800;
  font-size: 24px
}

.text-content {
  width: 400px;
  font-size: 13px;
  margin-top: 20px;
}

.text-learn {
  font-weight: 500;
  font-size: 14px;
  margin-top: 30px;
  z-index: 1;
  cursor: pointer;
  position: relative;
}

.text-underline {
  height: 10px;
  width: v-bind(underLine);
  border-radius: 10px;
  position: relative;
  bottom: 9px;
}

.left-learn {
  background-color: #fff7ba;
  transition: background-color 0.2s;
}

.text-learn:hover + .left-learn {
  background-color: #ffd004;
}

.right-learn {
  background-color: #fdd8d0;
  transition: background-color 0.2s;
}

.text-learn:hover + .right-learn {
  background-color: #f97461;
}
</style>