<template>
  <div><input type="text" v-model="use" />{{ use }}</div>
</template>
<script>
import { ref } from "@vue/composition-api";
export default {
  setup() {
    const use = ref("use");

    return {
      use
    };
  }
};
</script>
