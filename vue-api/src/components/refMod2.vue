<template>
  <div ref="use1">refmod2</div>
</template>
<script>
import { ref } from "@vue/composition-api";
export default {
  //refmod1调用refmod2
  setup() {
    const use1 = ref(123);
    return {
      use1
    };
  }
};
</script>
