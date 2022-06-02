<template>

  <div class="black-bg" v-if="모달창열렸니 == true">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
      <button @click="모달창열렸니 = false">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a v-for="loop in menu" :key="loop"> {{ loop }}</a>
  </div>

  <!-- <div v-for="(a,i) in products" :key="i">
    <h4>{{ a }}</h4>
    <p>50만워</p>
    <button @click="신고수[0]++">허위매물신고</button> 
    <span>신고수 : {{신고수[0]++}} </span> 
  </div> -->
  <div>
    <img src="https://d1774jszgerdmk.cloudfront.net/1024/a5866e28-a13b-438b-a16a-14da5e56d515" class="room-img">
    <h4 @click="모달창열렸니 = true">{{ apartments[0].title }}</h4>
    <p>{{ apartments[0].price }}원</p>
    <button @click="신고수[0]++">허위매물신고</button> <span>신고수 : {{신고수[0]}} </span>
  </div>
  <div>
    <img src="https://d1774jszgerdmk.cloudfront.net/1024/8c8bc2bd-570f-479b-a7f8-b08425405a95" class="room-img">
    <h4>{{ apartments[1].title }}</h4>
    <p>{{ apartments[1].price }}원</p>
    <button @click="신고수[1]++">허위매물신고</button> <span>신고수 : {{신고수[1]}} </span>
  </div>
  <div>
    <img src="https://d1774jszgerdmk.cloudfront.net/1024/61463a6a-6656-4a03-a7f7-34ce20b97dfe" class="room-img">
    <h4>{{ apartments[2].title }}</h4>
    <p>{{ apartments[2].price }}원</p>
    <button @click="신고수[2]++">허위매물신고</button> <span>신고수 : {{신고수[2]}} </span>
  </div>
</template>

<script>

import data from './assets/apartment-data.js';

export default {
  name: 'App',
  data() {
    return {
      apartments : data,
      모달창열렸니 : false,
      신고수 : [0, 0, 0],
      price : [60, 70, 80],
      menu : ['Home', 'Shop', 'About'],
      products :  ['역삼동원룸', '천호동원룸', '마포구원룸'],
    }
  },

  components: {
  }
}
</script>

<style>
body{
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed; padding: 20px;
}

.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}

.room-img {
  width: 100%;
  margin-top: 40px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
