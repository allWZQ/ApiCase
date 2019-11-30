<template>
  <div></div>
</template>
<script>
import { isRef, ref } from "@vue/composition-api";
export default {
  setup() {
    const count = ref(0);
    //判断
    const count2 = isRef(count) ? count.value : count;
    console.log(count.value);
    console.log(count2);
    return {
      count,
      count2
    };
  }
};
</script>
