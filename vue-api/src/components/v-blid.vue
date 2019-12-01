<template>
  <div>
    <input type="text" :value="use" />{{ use }}
    <br />
    <a :href="a1">网站1</a>
    <br />
    <span v-html="a2"></span>
  </div>
</template>
<script>
import { ref } from "@vue/composition-api";
export default {
  setup() {
    const use = ref("222222");
    const a1 = ref("www.baidu.com");
    const a2 = ref("<a href='www.baidu.com'>网站2</a>");
    return {
      use,
      a2,
      a1
    };
  }
};
</script>
