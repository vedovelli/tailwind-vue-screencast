<template>
  <div
    :class="{ hidden: !open }"
    class="z-30 absolute top-0 inset-x-0 max-w-3xl mx-auto w-full p-2 transition transform origin-top lg:hidden"
  >
    <div
      class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 bg-white divide-y divide-gray-200"
    >
      <div class="pt-3 pb-2">
        <div class="flex items-center justify-between px-4">
          <div>
            <img
              class="h-8 w-auto"
              src="https://tailwindui.com/img/logos/workflow-mark-cyan-600.svg"
              alt="Workflow"
            />
          </div>
          <div class="-mr-2">
            <button
              @click="handler()"
              type="button"
              class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-cyan-500"
            >
              <span class="sr-only">Close menu</span>
              <!-- Heroicon name: x -->
              <svg
                class="h-6 w-6"
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
        </div>
        <div class="mt-3 px-2 space-y-1">
          <a
            href="#"
            class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
            >Home</a
          >
          <a
            href="#"
            class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
            >Profile</a
          >
          <a
            href="#"
            class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
            >Resources</a
          >
          <a
            href="#"
            class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
            >Company Directory</a
          >
          <a
            href="#"
            class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
            >Openings</a
          >
        </div>
      </div>
      <div class="pt-4 pb-2">
        <div class="flex items-center px-5">
          <div class="flex-shrink-0">
            <img
              class="h-10 w-10 rounded-full"
              src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
              alt=""
            />
          </div>
          <div class="ml-3 min-w-0 flex-1">
            <div class="text-base font-medium text-gray-800 truncate">
              Rebecca Nicholas
            </div>
            <div class="text-sm font-medium text-gray-500 truncate">
              rebecca.nicholas@example.com
            </div>
          </div>
          <button
            class="ml-auto flex-shrink-0 bg-white p-1 text-gray-400 rounded-full hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-cyan-500"
          >
            <span class="sr-only">View notifications</span>
            <!-- Heroicon name: bell -->
            <svg
              class="h-6 w-6"
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
                d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
              />
            </svg>
          </button>
        </div>
        <div class="mt-3 px-2 space-y-1">
          <a
            href="#"
            class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
            >Your Profile</a
          >
          <a
            href="#"
            class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
            >Settings</a
          >
          <a
            href="#"
            class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
            >Sign out</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MobileMenu",
  props: {
    open: {
      type: Boolean,
      default: false,
    },
    handler: {
      type: Function,
      required: true,
    },
  },
};
</script>
