<template>
  <button @click="changeMessage">{{ message }}</button>
  {{ watchMessage }}
</template>

<script>
export default {
  data() {
    return {
      message: "안녕하세요 watch기능테스트 오리지널 문구",
      watchMessage: "",
    };
  },
  watch: {
    /* message란 변수를 지켜보고있다 변경이 있으면 실행
      데이터 뿐만 아니라 computed로 계산된 형태의 데이터도 watch로 감지할 수 있다.
      보통 게시판에서 한 컬럼을 선택하였을때, 고유한 id값이 바뀜을 감지하고
      이때, 그id값에 상세데이터를 호출할때 주로사용한다
    */
    message() {
      this.watchMessage = "watch 동작";
    },
    id() {
      //해당 상세데이터를 조회하는 api호출
    },
  },
  methods: {
    changeMessage() {
      console.log("함수호출");
      this.message = "변경된 message입니다";
    },
  },
};
</script>

<style></style>
