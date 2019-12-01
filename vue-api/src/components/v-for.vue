<template>
  <div>
    <div>{{ names[2] }}</div>
    <div>-------------------------------------</div>
    <div v-for="name in names" :key="name.id">{{ name }}</div>
    <div v-for="(nameAge, index) in nameAges" :key="nameAge.id">
      {{ index }}-{{ nameAge.name }}-{{ nameAge.age }}
    </div>
    <div>-------------------------------------</div>
    <div v-for="(nameAge, index) in nameAges" :key="nameAge.id">
      <p>{{ index }}-{{ nameAge.name }}</p>
      <i>{{ index }}-{{ nameAge.age }}</i>
    </div>
    <div>-------------------------------------</div>
    <div v-for="nameAge in nameAges" :key="nameAge.id">
      <div v-for="(name, age) in nameAge" :key="name.id">
        <p>{{ name }}-{{ age }}</p>
      </div>
    </div>
  </div>
</template>
<script>
import { ref, reactive } from "@vue/composition-api";
export default {
  setup() {
    const names = ref(["Hmbb", "Pdx", "Zyg"]);

    const nameAges = reactive([
      { name: "hmbb", age: 3 },
      { name: "Pdx", age: 0 },
      { name: "Zyg", age: 5 }
    ]);
    return {
      names,
      nameAges
    };
  }
};
</script>
