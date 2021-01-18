<template>
  <div class="absolute right-0 flex-shrink-0 lg:hidden">
    <!-- Mobile menu button -->
    <button
      @click="handler()"
      class="bg-transparent p-2 rounded-md inline-flex items-center justify-center text-cyan-200 hover:text-white hover:bg-white hover:bg-opacity-10 focus:outline-none focus:ring-2 focus:ring-white"
      aria-expanded="false"
    >
      <span class="sr-only">Open main menu</span>
      <!--
              Heroicon name: menu

              Menu open: "hidden", Menu closed: "block"
            -->
      <svg
        class="block h-6 w-6"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        aria-hidden="true"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M4 6h16M4 12h16M4 18h16"
        />
      </svg>
      <!--
              Heroicon name: x

              Menu open: "block", Menu closed: "hidden"
            -->
      <svg
        class="hidden h-6 w-6"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        aria-hidden="true"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M6 18L18 6M6 6l12 12"
        />
      </svg>
    </button>
  </div>
</template>

<script>
export default {
  name: "Hamburger",
  props: {
    handler: {
      type: Function,
      required: true,
    },
  },
};
</script>
