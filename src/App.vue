<
<template>
  <div>
    <!-- 인라인 핸들러-템플릿에서 처리
    <button @click="count++">인라인핸들러</button>
    <h1>{{ count }}</h1> -->
    <!-- 메소드 핸들러 - 스크립트에서 처리 -->
    <button @click="changeName">메소드핸들러</button>
    <h1>{{ name }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      name: "Vue.js",
    };
  },
  methods: {
    changeName() {
      this.name = "변경된 데이터입니다.";
    },
  },
};
</script>

<style></style>
>
