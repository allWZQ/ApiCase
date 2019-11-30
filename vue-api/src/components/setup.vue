<template>
  <div></div>
</template>
<script>
import {} from "@vue/composition-api";
export default {
  //对比setup调用时间
  //接收props
  props: {
    p: {
      type: String
    }
  },
  //context调用上下文的对象
  setup(props, context) {
    console.log("setup");
    console.log(props);
    console.log(context);
  },
  beforeCreate() {
    console.log("beforeCreate");
  },
  created() {
    //组件
    console.log("created");
  }
};
</script>
