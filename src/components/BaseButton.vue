<template>
  <div style="display: flex; gap: 8px; justify-content: center;">
    <button class="base-button" @click="addCount">
      Add number
    </button>
    <button class="base-button" @click="resetCount">
      Reset
    </button>
    <button class="base-button" @click="subCount">
      Sub number
    </button>
  </div>

  <Count ref="countRef"/>
</template>

<script>
import Count                             from "@/components/Count";
import {defineComponent, onMounted, ref} from "vue";

export default defineComponent({
  name      : "BaseButton",
  components: {Count},
  setup() {
    const countRef = ref(null)
    const addCount = () => {
      countRef.value.addNumber();
    };

    const resetCount = () => {
      countRef.value.resetNumber();
    };

    const subCount = () => {
      countRef.value.subNumber();
    };

    onMounted(() => {
      resetCount();
    })

    return {
      addCount,
      resetCount,
      subCount,
      countRef,
    };
  },
})
</script>

<style scoped>

</style>