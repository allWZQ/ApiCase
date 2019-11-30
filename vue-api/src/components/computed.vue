<template>
  <div>
    <p>{{ count }}</p>
    <p>{{ count2 }}</p>
    <button @click="add">+1</button>
  </div>
</template>
<script>
import { ref, computed } from "@vue/composition-api";
export default {
  setup() {
    const count = ref(0);

    const count2 = computed(() => count.value + 1); //计算结果count2也是一个ref（）对象
    //count2.value++ 无法改变数值
    //count2.value = 6; 无法赋值会报错
    const add = () => {
      count.value += 1;
    };
    //computed中的get，set方法
    const count3 = computed({
      //取值
      get: () => count.value + 1,
      //赋值
      set: val => {
        //此处的val 可以随便写，传入形参赋值的中间值
        count.value = val - 1;
      }
    });
    count3.value = 6;
    console.log(count.value); //5
    console.log(count3.value); //6
    return {
      count,
      count2,
      add,
      count3
    };
  }
};
</script>
