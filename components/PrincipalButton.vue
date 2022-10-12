<!-- Please remove this file from your project -->
<template>
  <button class="h-14 w-36 rounded-md border-2">{{ title }}</button>
</template>

<script>
export default {
  name: "Button",
  props: {
    title: String,
  },
};
</script>
