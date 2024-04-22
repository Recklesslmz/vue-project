<script setup lang="ts">
import { ref } from 'vue'

import testImg from '@/assets/test.jpg'

const activeNum = ref(0)

const imgList = [
  { id: 1, testImg },
  { id: 2, testImg },
  { id: 3, testImg }
]

const handleClick = (index: number) => {
  activeNum.value = index

  console.log(index)
}
</script>

<template>
  <div class="content">
    <div class="main">
      <div class="left">
        <div class="goodList">
          <img
            @click="handleClick(index)"
            class="imgUrl"
            :class="{ active: activeNum === index }"
            v-for="(item, index) in imgList"
            :key="item.id"
            :src="item.testImg"
          />
        </div>
        <div class="mainGood">
          <img class="mainImgUrl" :src="testImg" />
        </div>
      </div>
      <div class="middle">
        <div class="desc">
          New Arrival Cheap USB 3D Mouse up to 7200 Dpi LED RGB Wired Optical Gamer PC Mice Computer
          Office Gaming Mouse for Game
        </div>
        <div class="line"></div>
        <div class="price">
          <div class="priceState">
            <span class="num">US$7.00</span>
            <span class="unit">
              <span class="number">1-99 </span>
              <span class="content">Pieces</span>
            </span>
          </div>
          <div class="priceLine" />
          <div class="priceState">
            <span class="num">US$7.00</span>
            <span class="unit">
              <span class="number">1-99 </span>
              <span class="content">Pieces</span>
            </span>
          </div>
          <div class="priceLine" />
          <div class="priceState">
            <span class="num">US$7.00</span>
            <span class="unit">
              <span class="number">1-99 </span>
              <span class="content">Pieces</span>
            </span>
          </div>
          <div class="priceState">
            <span class="num">US$7.00</span>
            <span class="unit">
              <span class="number">1-99 </span>
              <span class="content">Pieces</span>
            </span>
          </div>
          <div class="priceLine" />
          <div class="priceState">
            <span class="num">US$7.00</span>
            <span class="unit">
              <span class="number">1-99 </span>
              <span class="content">Pieces</span>
            </span>
          </div>
        </div>
        <div class="btnState">
          <button class="btn">Send Inquiry</button>
        </div>
      </div>
      <div class="right"></div>
    </div>
    <div class="contentline" />
    <div class="bottom">
      <div class="title">Similar Products</div>
      <div class="bottomMain">
        <div class="bottomContent">
          <div class="bottomGood">
            <div class="bottomImg">
              <img class="bottomImgUrl" :src="testImg" />
            </div>
            <span class="bottomImgDesc">
              Product name product name product name product name product name...
            </span>
          </div>
        </div>
        <div class="bottomContent">
          <div class="bottomGood">
            <div class="bottomImg">
              <img class="bottomImgUrl" :src="testImg" />
            </div>
            <span class="bottomImgDesc">
              Product name product name product name product name product name...
            </span>
          </div>
        </div>
        <div class="bottomContent">
          <div class="bottomGood">
            <div class="bottomImg">
              <img class="bottomImgUrl" :src="testImg" />
            </div>
            <span class="bottomImgDesc">
              Product name product name product name product name product name...
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.main {
  display: flex;
}
.goodList {
  display: flex;
  flex-direction: column;
}
.left {
  display: flex;
}
.imgUrl {
  width: 50px;
  height: 50px;
  border-radius: 3px;
  border: 1px solid #e6ecf2;
}
.imgUrl:not(:first-child) {
  margin-top: 13px;
}
.active {
  border: 2px solid #555;
}
.mainGood {
  width: 300px;
  height: 300px;
  background: rgba(0, 0, 0, 0.03);
  margin-left: 11px;
}
.mainImgUrl {
  width: 300px;
  height: 300px;
  border-radius: 4px;
}
.middle {
  display: flex;
  flex-direction: column;
  width: 849px;
  margin-left: 30px;
}
.desc {
  font-size: 18px;
  font-weight: normal;
  line-height: 26px;
  letter-spacing: 0px;
  overflow: hidden;
  text-overflow: ellipsis;
  -webkit-line-clamp: 2;
  color: #000000;
}
.line {
  width: 849px;
  height: 1px;
  background: #e6ecf2;
  margin-top: 11px;
}
.price {
  display: flex;
  margin-top: 15px;
}
.num {
  display: block;
  font-size: 20px;
  font-weight: 500;
  line-height: 26px;
  color: #e64545;
}
.number {
  color: #222222;
}
.content {
  color: #888888;
}
.unit {
  font-family: Roboto;
  font-size: 14px;
  font-weight: normal;
  line-height: 21px;
  display: block;
  margin-top: 3px;
}
.priceLine {
  width: 1px;
  height: 40px;
  background: #e6ecf2;
  margin-left: 20px;
  margin-right: 20px;
  position: relative;
  top: 5px;
}
.btn {
  width: 177px;
  height: 31px;
  border-radius: 1000px;
  border: none;
  background: #e64545;
  color: #fff;
  font-size: 14px;
  line-height: 21px;
  margin-top: 25px;
}
.btn:hover {
  cursor: pointer;
  background: #cf3e3e;
}
.contentline {
  width: 1916px;
  height: 1px;
  background: #e6ecf2;
  margin-top: 20px;
}
.bottomContent {
  display: flex;
  margin-left: 15px;
  margin-top: 10px;
}
.bottomContent {
  width: 288px;
  height: 335px;
  padding: 15px;
}
.bottomContent:hover {
  width: 288px;
  height: 335px;
  box-shadow: 0px 3px 6px -3px rgba(0, 0, 0, 0.12), 0px 6px 10px 0px rgba(0, 0, 0, 0.06),
    0px 9px 16px 8px rgba(0, 0, 0, 0.03);
}
.title {
  font-size: 18px;
  font-weight: 500;
  line-height: 26px;
  color: #222222;
  margin-top: 14.5px;
}
.bottomImg {
  width: 89.58%;
  height: 77.01%;
}
.bottomImgUrl {
  width: 89.58%;
  height: 77.01%;
}
.bottomImgDesc {
  font-size: 14px;
  font-weight: normal;
  line-height: 21px;
  color: #222222;
}
.bottomMain {
  display: flex;
}
</style>
