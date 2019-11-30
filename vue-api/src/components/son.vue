<template>
  <div>
    <div :style="{ color: color }">子组件</div>
    <grandson />
  </div>
</template>
<script>
import grandson from "./grandson";
import { inject } from "@vue/composition-api";
export default {
  components: {
    grandson
  },
  setup() {
    //inject 注入,子组件通过调用父组件提供的themeColor，继承父组件
    const color = inject("themeColor");
    return {
      color
    };
  }
};
</script>
