<template>
  <div class="h-screen flex flex-col justify-between">
    <TheMenu />
    <NuxtChild />
  </div>
</template>
<script>
import TheMenu from "@/components/TheMenu.vue";
export default {
  components: {
    TheMenu,
  },
};
</script>
<style></style>
