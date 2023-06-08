<script setup>
import { ref } from "vue";

const dataList = ref([
  "메모 1 내용",
  "메모 2 내용",
  "메모 3 내용",
  "메모 4 내용",
  "메모 5 내용",
]);

function add() {
  dataList.push("추가된 내용");
}
</script>
<template>
  <div class="memo">
    <div class="act">
      <button class="btn btn-primary" @click="add()">+ 추가</button>
    </div>

    <ul>
      <li v-for="(data, index) in dataList" :key="index">{{ data }}</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.memo {
  .act {
    padding: 10px 10px 5px 5px;
    text-align: right;
  }
  ul {
    list-style: none;
    padding: 0;
    margin: 0;

    li {
      padding: 5px 10px;
      margin: 5px;
    }
  }
}
</style>
