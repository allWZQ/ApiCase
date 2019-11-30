<template>
  <div>
    <button @click="stopwatch">停止watch</button>
  </div>
</template>
<script>
import { ref, watch } from "@vue/composition-api";
export default {
  setup() {
    const count = ref(2);
    //清除watch
    const stop = watch(() => console.log(count.value));

    setTimeout(() => {
      count.value += 1;
    }, 1500);
    const stopwatch = () => {
      //清除watch调用stop()方法即可
      stop();
    };
    return {
      count,
      stop,
      stopwatch
    };
  }
};
</script>
