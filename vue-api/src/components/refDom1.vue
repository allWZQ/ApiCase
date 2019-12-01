<template>
  <div>
    <span ref="color"><I>我不是红色</I></span>
    <br />
    <button @click="useRef">使用组件</button>
    <refMod2 ref="use2" />
  </div>
</template>
<script>
import refMod2 from "./refMod2";
import { ref, onMounted } from "@vue/composition-api";
export default {
  components: {
    refMod2
  },
  setup() {
    //引用元素
    const color = ref(null);

    //引用组件
    const use2 = ref(null);

    const useRef = () => {
      console.log(use2);
      console.log(use2.value.use1);
      use2.value.use1.style.color = "red";
    };
    //在生命周期挂载完成执行加载
    onMounted(() => {
      color.value.style.color = "red";
    });

    return {
      color,
      useRef,
      use2
    };
  }
};
</script>
