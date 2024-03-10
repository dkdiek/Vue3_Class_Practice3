<template>
  <div>
    <input type="text" name="" id="" v-model="inputValue1" />
    {{ inputValue1 }}
  </div>
  <div>
    <!-- 한글은 아래와 같이 반영해야 바로바로 보인다 -->
    <input
      type="text"
      :value="inputValue2"
      @input="inputValue2 = $event.target.value"
    />
    {{ inputValue2 }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputValue1: "",
      inputValue2: "",
    };
  },
};
</script>

<style></style>
