<template>
  <div>{{ sendProps1 }}</div>
  <div>{{ sendProps2 }}</div>
  <div>{{ sendProps3.id }}</div>
  <div>{{ sendProps3.name }}</div>
</template>

<script setup lang="ts">
import { toRefs } from "vue";

interface Obj {
  id: number;
  name: string;
}

//1.컴포지션 api에서 타입스크립트를 활용하는 방법
//1-1 prop 받은 데이터 형식에 맞게 타입을 지정해준다

//Prop 받은 데이터 이름 자체에 미리 선언해둔 타입을 설정해준다.
interface Props {
  sendProps1: String;
  sendProps2: Number;
  sendProps3: Obj;
}

//definProps toRefs 내장함수를 통해 Prop 받은 데이터를 활용하여 템플릿 부분에 호출하여 사용한다.
/* define props는 import안해도 vue가 알아서 해준다 */
const props = defineProps<Props>();
//torefs를 안하면 template에서 props.sendProps1 이런식으로 써야한다
const { sendProps1, sendProps2, sendProps3 } = toRefs(props);
</script>

<style></style>
