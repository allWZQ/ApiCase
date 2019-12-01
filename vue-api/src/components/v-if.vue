<template>
  <div>
    <button @click="error = !error">Toggle error</button>
    <button @click="success = !success">Toggle success</button>
    <p v-if="error">404</p>
    <p v-else-if="success">200</p>
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
