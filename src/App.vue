<template>
  <div class="black-bg" v-if="isModal">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세내용</p>
      <button @click="isModal = false">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a v-for="(메뉴, i) in 메뉴들" :key="i"> {{ 메뉴 }} </a>
  </div>
  <div class="room_wrapper">
    <img src="./assets/room0.jpg" />
    <h4 @click="isModal = !isModal">{{ products[0] }}</h4>
    <p>10만원</p>
    <button @click="increase(0)">허위매물 신고</button>
    <span>신고수 : {{ count[0] }}</span>
  </div>
  <div class="room_wrapper">
    <img src="./assets/room1.jpeg" />
    <h4>{{ products[1] }}</h4>
    <p>10만원</p>
    <button @click="increase(1)">허위매물 신고</button>
    <span>신고수 : {{ count[1] }}</span>
  </div>
  <div class="room_wrapper">
    <img src="./assets/room2.jpg" />
    <h4>{{ products[2] }}</h4>
    <p>10만원</p>
    <button @click="increase(2)">허위매물 신고</button>
    <span>신고수 : {{ count[2] }}</span>
  </div>

  <!-- <div v-for="(p, i) in products" :key="i">
    <h4>{{ p }}</h4>
    <p>10만원</p>
    <button @click="increase(i)">허위매물 신고</button>
    <span>신고수 : {{ count[i] }}</span>
  </div> -->
</template>

<script>
import oneroom from "./oneroom";

export default {
  data() {
    return {
      isModal: false,
      count: [0, 0, 0],
      메뉴들: ["home", "shop", "about"],
      products: ["역삼동 원룸", "천호동 원룸", "삼성동 원룸"],
      onerooms: oneroom,
    };
  },
  methods: {
    increase(i) {
      this.count[i]++;
    },
  },
};
</script>

<style>
.menu {
  background-color: darkslateblue;
  padding: 15px;
  border-radius: 5px;
  display: flex;
  justify-content: space-evenly;
}

.menu a {
  color: white;
  padding: 10px;
}

.room_wrapper img {
  width: 200px;
  height: 150px;
}

body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: white;
  padding: 20px;
}
</style>
