<template>
  <div :style="{ color: color }">孙组件</div>
</template>
<script>
import { inject } from "@vue/composition-api";
export default {
  setup() {
    //inject 注入,孙组件通过调用父组件提供的themeColor，继承父组件
    const color = inject("themeColor");
    return {
      color
    };
  }
};
</script>
