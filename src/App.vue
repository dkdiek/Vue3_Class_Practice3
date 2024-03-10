<template>
  <childComponent
    :sendProps1="title"
    :sendProps2="createAt"
    :sendProps3="obj"
  />
</template>
<!-- 컴포지션 api는 setup이란게 붙어야함 -->
<script setup lang="ts">
import { reactive, ref } from "vue";
import ChildComponent from "./components/ChildComponent.vue";

interface Obj {
  id: number;
  name: string;
}

const title = ref("부모컴포넌트에서 선언된 데이터입니다.");
const createAt = ref<nubmer>(2024);
const obj = reactive<Obj>({
  id: 2024,
  name: "john",
});
</script>

<style></style>
