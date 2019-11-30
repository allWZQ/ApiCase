<template>
  <div></div>
</template>
<script>
import { reactive, watch, ref } from "@vue/composition-api";
export default {
  setup() {
    //监视多个reactive数据源
    const state = reactive({ count: 1, name: "wzq" });

    watch(
      [() => state.count, () => state.name],
      ([newcount, newname], [oldcount, oldname]) => {
        console.log(newcount, newname);
        console.log(oldcount, oldname);
      },
      {
        lazy: true
      }
    );

    setTimeout(() => {
      state.count += 1;
    }, 2000);

    setTimeout(() => {
      state.name += "最帅";
    }, 3000);

    //监视多个ref数据源
    const count2 = ref(12);
    const conut3 = ref(13);

    watch(
      [count2, conut3],
      ([newcount2, newcount3], [oldname2, oldname3]) => {
        console.log(newcount2, newcount3);
        console.log(oldname2, oldname3);
      },
      {
        lazy: true
      }
    );

    setTimeout(() => {
      count2.value += 1;
    }, 4000);
    setTimeout(() => {
      conut3.value += 1;
    }, 5000);
    return {
      state,
      count2,
      conut3
    };
  }
};
</script>
