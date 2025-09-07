<template>
  <div class="menu">
    <!-- v-for 반복문 -->
    <!-- 이름 in 횟수(데이터) => 데이터가 들어가면 데이터의 길이만큼 반복 -->
    <a v-for="(menu, i) in menus" :key="i">{{ menu }}</a>
  </div>
  <div>
    <h4>{{ products[0] }}</h4>
    <p>110 만원</p>
    <button @click="counts[0]++">허위매물 신고</button>
    <span>신고수 : {{ counts[0] }}</span>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>70 만원</p>
    <button @click="counts[1]++">허위매물 신고</button>
    <span>신고수 : {{ counts[1] }}</span>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>100 만원</p>
    <button @click="counts[2]++">허위매물 신고</button>
    <span>신고수 : {{ counts[2] }}</span>
  </div>
</template>

<script>
export default {
  name: "App",
  // 데이터 바인딩
  // data 보관함 - data는 object형식으로 저장
  data() {
    return {
      counts: [0, 0, 0],
      menus: ["Home", "Shop", "About"],
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
    };
  },
  // 함수
  methods: {
    increase() {
      this.count++;
    },
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
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
