<template>
  <div id="vue" class="counter">
    <button @click="subtract()" class="btn">-</button>
    <pre>VUE: {{ count }}</pre>
    <button @click="add()" class="btn">+</button>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const count = ref(0);
    const add = () => (count.value = count.value + 1);
    const subtract = () => (count.value = count.value - 1);

    return {
      count,
      add,
      subtract,
    };
  },
};
</script>

<style scoped lang="scss">
.btn {
  @apply mx-auto my-auto text-white bg-green-600 py-2 px-4 focus:outline-none hover:bg-green-800 rounded text-sm;
}
</style>
