<template>
  <div></div>
</template>
<script>
import { ref, watch, reactive } from "@vue/composition-api";
export default {
  setup() {
    //监视ref类型的数据
    const count = ref(0);
    //无新值，旧值，会打印初始值
    watch(() => console.log(count.value));
    //有新值，旧值
    watch(
      count,
      (newVal, oldVal) => {
        console.log(newVal, oldVal);
      },
      { lazy: true } //可以添加lazy: true
    );
    setTimeout(() => {
      count.value += 1;
    }, 1500);

    //监视reactive类型的数据
    const state = reactive({
      count: 2
    });

    watch(
      () => state.count,
      (newVal, oldVal) => {
        //newVal是新的值，oldVal是旧的值，
        //这两个参数可以随便取名
        console.log(newVal, oldVal);
      },
      {
        lazy: true //当lazy为true的时候，组件的初始值不会被执行
      }
    );

    setTimeout(() => {
      state.count += 1;
    }, 1500);

    return {
      count,
      state
    };
  }
};
</script>
