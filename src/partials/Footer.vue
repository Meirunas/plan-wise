<template>
  <footer class="border-t border-slate-800 py-8">
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <!-- Logo and Icons aligned -->
      <div class="flex justify-between items-center">
        <!-- Logo -->
        <Logo />

        <!-- Social Icons -->
        <ul class="flex space-x-4">
          <li>
            <span
              href="javascript:void(0)"
              aria-label="Twitter"
              class="text-indigo-500 hover:text-slate-300 transition"
            >
              <svg
                class="w-8 h-8 fill-current "
                viewBox="0 0 32 32"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="m13.063 9 3.495 4.475L20.601 9h2.454l-5.359 5.931L24 23h-4.938l-3.866-4.893L10.771 23H8.316l5.735-6.342L8 9h5.063Z"
                />
              </svg>
            </span>
          </li>
          <li>
            <span
              href=""
              aria-label="Medium"
              class="text-indigo-500 hover:text-slate-300 transition "
            >
              <svg
                class="w-8 h-8 fill-current"
                viewBox="0 0 32 32"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M23 8H9a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h14a1 1 0 0 0 1-1V9a1 1 0 0 0-1-1Zm-1.708 3.791-.858.823a.251.251 0 0 0-.1.241V18.9a.251.251 0 0 0 .1.241l.838.823v.181h-4.215v-.181l.868-.843c.085-.085.085-.11.085-.241v-4.887l-2.41 6.131h-.329l-2.81-6.13V18.1a.567.567 0 0 0 .156.472l1.129 1.37v.181h-3.2v-.181l1.129-1.37a.547.547 0 0 0 .146-.472v-4.749a.416.416 0 0 0-.138-.351l-1-1.209v-.181H13.8l2.4 5.283 2.122-5.283h2.971Z"
                />
              </svg>
            </span>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  components: {
    Logo,
  },
};

import Logo from "../partials/Logo.vue";
</script>
