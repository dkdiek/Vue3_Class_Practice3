<template>
  <div>
    {{ count }}
  </div>
  <h1>Vue js 라이프사이클 테스트</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  //컴포넌트 생성전 data, mehtods에 선언한 데이터,함수에 접근불가
  beforeCreate() {
    console.group("lifcycle is beforecreate", this.count);
  },
  //컴포넌트가 생성된 직후 접근할 수 있는 라이프 사이클 훅. 초기화 이후 data접근, 메소드 접근가능
  created() {
    console.group("lifcycle is created", this.count);
    this.test();
  },
  //mounted 컴포넌트,템플릿,렌더링된 dom에 접근 가능 dom 수정을 위해 사용 template 부분의 hteml element가 모두 렌더링된 후에 접근 가능
  //h1 셀렉트 못함
  // beforeMount() {
  //   console.group("lifcycle is beforeMount", document.querySelector("h1"));
  // },
  // //h1 셀렉트 가능
  // mounted() {
  //   console.group("lifcycle is mounted", document.querySelector("h1"));
  // },
  //메소드
  methods: {
    test() {
      console.log("함수호출");
    },
  },
};
</script>

<style></style>
