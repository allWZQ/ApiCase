<template>
  <div>
    <input type="text" v-model="count" />
  </div>
</template>
<script>
import { ref, watch } from "@vue/composition-api";
export default {
  setup() {
    const count = ref("");
    //在控制台读取val
    const asyncprint = val => {
      //延迟打印 ,必须将setTimeout return出去，不然外面调用不到
      return setTimeout(() => {
        console.log(val);
      }, 1000);
    };
    watch(
      count,
      (newcount, oldcount, clear) => {
        //将newcount作为参数传给val
        const timerId = asyncprint(newcount);
        //清除之前的异步任务
        clear(() => clearTimeout(timerId));
      },
      { lazy: true }
    );
    return {
      count
    };
  }
};
</script>
