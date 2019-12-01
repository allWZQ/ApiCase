<template>
  <div>
    <button @click="update" ref="color">生命周期更新</button>
  </div>
</template>
<script>
import {
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
  ref
} from "@vue/composition-api";
export default {
  setup() {
    const color = ref("red");

    const update = () => {
      color.value.style.color = "red";
    };
    console.log("组件实例化完毕，但页面未显示");
    onBeforeMount(() => {
      console.log("组件挂载前，页面仍未展示，但是虚拟Dom已经配置");
    });
    onMounted(() => {
      console.log("组件挂载后，此方法执行后，页面显示");
    });
    onBeforeUpdate(() => {
      console.log("组件更新前，页面仍未更新，但是虚拟Dom已经配置");
    });
    onUpdated(() => {
      console.log("组件更新，此方法执行后，页面显示");
    });
    onBeforeUnmount(() => {
      console.log("组件销毁前");
    });
    onUnmounted(() => {
      console.log("组件销毁后");
    });
    return {
      color,
      update
    };
  }
};
</script>
