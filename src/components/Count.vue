<template>
  <div class="count">
    <h1>Count: {{ count }}</h1>
  </div>
</template>

<script>
import {defineComponent, ref} from "vue";

export default defineComponent({
  name: "Count",
  setup(_, context) {
    const count = ref();

    const addNumber = () => {
      count.value++;
    };

    const resetNumber = () => {
      count.value = 0;
    };

    const subNumber = () => {
      count.value--;
    };

    context.expose({addNumber, resetNumber, subNumber})

    return {
      count,
    }
  },
})
</script>

<style scoped>

</style>