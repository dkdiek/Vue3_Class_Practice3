<!-- v-for -->
<template>
  <div>
    <!-- v-for에서 받은 index를 key값으로 쓰면안된다 데이터를 추가하면 해당 자리의 local 데이터가 남는다 -->
    <!-- array-->
    <li v-for="(array, index) in sampleArray" :key="array">
      {{ index }}번은 {{ array }}
    </li>
    <!-- object-->
    <li v-for="item in otherArray" :key="item.id">
      {{ item.id }}번 학생은 {{ item.name }}
    </li>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sampleArray: ["a", "b", "c", "d"],
      otherArray: [
        { id: 0, name: "John" },
        { id: 1, name: "kim" },
        { id: 2, name: "lee" },
        { id: 3, name: "park" },
      ],
    };
  },
};
</script>

<style></style>
>
