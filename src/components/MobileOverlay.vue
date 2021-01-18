<template>
  <div
    :class="{ hidden: !open }"
    class="z-20 fixed inset-0 bg-black bg-opacity-25 lg:hidden"
    aria-hidden="true"
  ></div>
</template>

<script>
export default {
  name: "MobileOverlay",
  props: {
    open: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
