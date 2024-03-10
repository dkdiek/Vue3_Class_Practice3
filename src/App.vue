<template>
  <!-- 선언적 렌더링 -->
  <div>{{ rawHtml }}</div>
  <div>{{ rawHtml2 }}</div>
  <!-- html 코드를 적용시켜 출력하려면 v-html 디렉티브사용 -->
  <div v-html="rawHtml2"></div>
  <!-- v-bind class isActive 변수가 true면 active class 적용 false면 미적용-->
  <h2 :class="{ active: isActive }">111</h2>
  <button @click="change">버튼</button>
  <!-- 스타일바인딩 -->
  <h3 style="color: red; font-size: 24px">스타일 바인딩 테스트</h3>
  <h3 :style="{ color: fontColor, fontSize: fontSize + 'px' }">
    스타일 바인딩 테스트
  </h3>
</template>

<script>
export default {
  data() {
    return {
      rawHtml: "이것은 텍스트입니다",
      rawHtml2: "<span style='color: red'>이것은 빨간색이어야 합니다.</span>",
      isActive: false,
      fontColor: "blue",
      fontSize: 48,
    };
  },
  methods: {
    change() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
h2.active {
  color: green;
}
</style>
