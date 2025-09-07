<template>
  <div class="menu">
    <!-- v-for 반복문 -->
    <!-- 이름 in 횟수(데이터) => 데이터가 들어가면 데이터의 길이만큼 반복 -->
    <a v-for="(menu, i) in menus" :key="i">{{ menu }}</a>
  </div>
  <div v-for="(product, i) in products" :key="i">
    <h4>{{ product.name }}</h4>
    <p>{{ product.price }}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  // 데이터 바인딩
  // data 보관함 - data는 object형식으로 저장
  data() {
    return {
      menus: ["Home", "Shop", "About"],
      products: [
        { name: "역삼동원룸", price: "110만원" },
        { name: "천호동원룸", price: "80만원" },
        { name: "마포구원룸", price: "100만원" },
      ],
    };
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
