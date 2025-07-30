<template>
  <header class="absolute w-full z-30">
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="flex items-center justify-between h-16 md:h-20">
        <!-- Site branding -->
        <div class="shrink-0 mr-4">
          <!-- Logo -->
          <Logo />
        </div>

        <!-- Desktop navigation -->
        <nav class="flex grow">
          <!-- Desktop sign in links -->
          <ul class="flex grow justify-end flex-wrap items-center">
            <li>
              <router-link
                class="font-medium text-slate-500 hover:text-slate-300 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out"
                to="/signin"
              >
                Sign in
              </router-link>
            </li>

            <!-- Register -->
            <li class="ml-3">
              <router-link
                class="btn-sm text-white bg-indigo-500 hover:bg-indigo-600 w-full shadow-xs group"
                to="/register"
              >
                Sign Up
                <span
                  class="tracking-normal text-sky-300 group-hover:translate-x-0.5 transition-transform duration-150 ease-in-out ml-1"
                  >-&gt;</span
                >
              </router-link>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  components: {
    Logo,
  },
};
import Logo from "../partials/Logo.vue";
</script>
