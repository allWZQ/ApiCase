<template>
  <div>
    <div>父组件</div>
    <button @click="color = 'red'">红色</button>
    <button @click="color = 'yellow'">黄色</button>
    <button @click="color = 'blue'">蓝色</button>
    <son />
  </div>
</template>
<script>
import { provide, ref } from "@vue/composition-api";
import son from "./son";
export default {
  components: {
    son
  },
  setup() {
    const color = ref("red");
    //provide提供 （组件名称，样式）
    provide("themeColor", color);
    return {
      color
    };
  }
};
</script>
