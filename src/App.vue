<
<template>
  <div>
    <h1>{{ text }}</h1>
    <!-- method는 3번 실행된다 -->
    <h1>changeText 함수 호출 값:{{ changeText() }}</h1>
    <h1>changeText 함수 호출 값:{{ changeText() }}</h1>
    <h1>changeText 함수 호출 값:{{ changeText() }}</h1>
    <!-- computed는 함수 모양이지만 데이터이기때문에 ()붙이지않는다 -->
    <!-- computed는 한번만 실행된다 -->
    <h2>{{ computedText }}</h2>
    <h2>{{ computedText }}</h2>
    <h2>{{ computedText }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "Computed test data",
    };
  },
  // method 부분에 선언된 함수와 동일한 로직일때,
  // 캐싱 기능이 없는 methods는 호출될때마다 console값이 출력되었음
  computed: {
    computedText() {
      console.log("computed call");
      console.log(this.text);

      return this.text.split("").reverse().join("");
    },
  },
  methods: {
    changeText() {
      console.log("function call");
      console.log(this.text);

      return this.text.split("").reverse().join("");
    },
  },
};
</script>

<style></style>
>
