<template>
  부모컴포넌트 레이아웃
  <!-- 자식컴포넌트에서 emit한걸 send-even로 받는다 parentEvent를 실행한다 -->
  <childComponent @send-event="parentEvent" />
</template>
<!-- 컴포지션 api는 setup이란게 붙어야함 -->
<script setup lang="ts">
import ChildComponent from "./components/ChildComponent.vue";

const parentEvent = (event: string) => {
  console.log(event);
};
</script>

<style></style>
