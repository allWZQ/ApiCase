<template>
  <div>
    <setup p="接收我" />
    <reactive />
    <ref />
    <isRef />
    <toRefs />
    <computed />
    <watch1 />
    <watch2 />
    <watch3 />
    <watch4 />
    <father />
  </div>
</template>
<script>
import setup from "../components/setup";
import reactive from "../components/reactive";
import ref from "../components/ref";
import isRef from "../components/isRef";
import toRefs from "../components/toRefs";
import computed from "../components/computed";
import watch1 from "../components/watch1";
import watch2 from "../components/watch2";
import watch3 from "../components/watch3";
import watch4 from "../components/watch4";
import father from "../components/father";
export default {
  name: "home",
  components: {
    setup,
    reactive,
    ref,
    isRef,
    toRefs,
    computed,
    watch1,
    watch2,
    watch3,
    watch4,
    father
  }
};
</script>
