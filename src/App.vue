<template>
  <div>
    <!-- 조건부 렌더링 -->
    <!-- <div v-if="isVisible" class="red"></div>
    <div v-if="isVisible === true" class="blue"></div>
    <div v-else class="black"></div> -->
    <!--  -->
    <!-- <div v-if="count > 1" class="red"></div>
    <div v-else class="blue"></div>
    <button @click="count++">증가 버튼</button>
    <button @click="count--">감소 버튼</button> -->

    <!-- v-show는 조건에 관계없이 렌더링되고 false일때는 display만 none으로 설정하여 안보임 -->
    <div v-show="isVisible" class="blue"></div>
    <div v-show="!isVisible" class="red"></div>
    <!-- v-if는 조건이 거짓이면 렌더링X -->
    <div v-if="isVisible" class="black"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false,
      count: 0,
    };
  },
};
</script>

<style>
.blue {
  width: 100px;
  height: 100px;
  background-color: blue;
}
.red {
  width: 100px;
  height: 100px;
  background-color: red;
}
.black {
  width: 100px;
  height: 100px;
  background-color: black;
}
</style>
>
