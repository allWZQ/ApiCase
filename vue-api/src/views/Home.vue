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
    <refDom1 />
    <nextTick />
    <vModel />
    <vBlid />
    <vIf />
    <vShow />
    <vFor />
    <liveCycle />
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
import refDom1 from "../components/refDom1";
import nextTick from "../components/nextTick";
import vModel from "../components/v-model";
import vBlid from "../components/v-blid";
import vIf from "../components/v-if";
import vShow from "../components/v-show";
import vFor from "../components/v-for";
import liveCycle from "../components/liveCycle";
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
    father,
    refDom1,
    nextTick,
    vModel,
    vBlid,
    vIf,
    vShow,
    vFor,
    liveCycle
  }
};
</script>
