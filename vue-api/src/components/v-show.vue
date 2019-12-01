<template>
  <div>
    <button @click="error = !error">toggle error</button>
    <button @click="success = !success">toggle success</button>
    <p v-show="error">404</p>
    <p v-show="success">200</p>
  </div>
</template>
<script>
import { ref } from "@vue/composition-api";
export default {
  setup() {
    const error = ref(false);
    const success = ref(false);
    return {
      error,
      success
    };
  }
};
</script>
