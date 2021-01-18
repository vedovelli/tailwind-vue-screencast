<template>
  <div class="ml-4 relative flex-shrink-0">
    <div>
      <button
        @click="toggleProfileMenu()"
        type="button"
        class="bg-white rounded-full flex text-sm ring-2 ring-white ring-opacity-20 focus:outline-none focus:ring-opacity-100"
        id="user-menu"
        aria-haspopup="true"
      >
        <span class="sr-only">Open user menu</span>
        <img
          class="h-8 w-8 rounded-full"
          src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
          alt=""
        />
      </button>
    </div>
    <!--
              Profile dropdown panel, show/hide based on dropdown state.

              Entering: ""
                From: ""
                To: ""
              Leaving: "transition ease-in duration-75"
                From: "transform opacity-100 scale-100"
                To: "transform opacity-0 scale-95"
            -->
    <div
      :class="{ hidden: !profileMenu.open }"
      class="origin-top-right z-40 absolute -right-2 mt-2 w-48 rounded-md shadow-lg py-1 bg-white ring-1 ring-black ring-opacity-5"
      role="menu"
      aria-orientation="vertical"
      aria-labelledby="user-menu"
    >
      <a
        href="#"
        class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
        role="menuitem"
        >Your Profile</a
      >
      <a
        href="#"
        class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
        role="menuitem"
        >Settings</a
      >
      <a
        href="#"
        class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
        role="menuitem"
        >Sign out</a
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfileDropdown",
  data() {
    return {
      profileMenu: {
        open: false,
      },
    };
  },
  methods: {
    toggleProfileMenu() {
      this.profileMenu.open = !this.profileMenu.open;
    },
  },
};
</script>
