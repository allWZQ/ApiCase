<template>
  <div>
    <button v-if="isshowinput === false" @click="showinpt">展示文本框</button>
    <input type="text" v-else ref="ipt" />
  </div>
</template>
<script>
import { ref } from "@vue/composition-api";
export default {
  setup() {
    const isshowinput = ref(false);

    const ipt = ref(null);
    const showinpt = () => {
      isshowinput.value = true;
    };
    return {
      isshowinput,
      showinpt,
      ipt
    };
  }
};
</script>
