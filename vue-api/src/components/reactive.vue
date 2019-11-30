<template>
  <div>
    <div>{{ count }}</div>
    <button @click="count += 1">+1</button>
  </div>
</template>
<script>
import { reactive } from "@vue/composition-api";
export default {
  setup() {
    //ractive用来声明一个响应式的对象
    //声明一个count:0 的对象
    const state = reactive({
      count: 0
    });
    console.log(state); //0
    state.count += 1;
    console.log(state); //1
    return state;
  }
};
</script>
