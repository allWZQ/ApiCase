<template>
  <div>
    <div>{{ count }}-----{{ name }}</div>
    <button @click="count++">+1</button>
  </div>
</template>
<script>
import { ref, reactive } from "@vue/composition-api";
export default {
  setup() {
    const count = ref(0);
    const state = reactive({
      count //相当于count:0
    });
    //再次创建一个ref为count2
    const count2 = ref(9);
    //将旧的ref 替换为新的ref
    state.count = count2;
    console.log(count.value);
    count.value++;
    console.log(state.count);
    console.log(count.value);
    return {
      count,
      count2,
      state,
      name: ref("wzq")
    };
  }
};
</script>
