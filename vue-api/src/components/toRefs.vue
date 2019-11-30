<template>
  <div>
    <p>{{ count }}</p>
    <button @click="add">+1</button>
  </div>
</template>
<script>
import { reactive, toRefs } from "@vue/composition-api";
export default {
  setup() {
    const state = reactive({
      count: 0,
      name: "wzq"
    });
    const add = () => {
      state.count += 1;
    };
    return {
      //...state 表示state里面包含了count和name，但state里的数据不再是响应式，且值变为固定的值
      ...toRefs(state), //将state里的值的值变成了ref形式的数据
      add
    };
  }
};
</script>
