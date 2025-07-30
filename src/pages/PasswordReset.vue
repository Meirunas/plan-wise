<template>
  <div class="flex flex-col min-h-screen overflow-hidden">
    <!-- Site header -->
    <header class="absolute w-full z-30">
      <div class="max-w-6xl mx-auto px-4 sm:px-6">
        <div class="flex items-center justify-between h-16 md:h-20">
          <!-- Site branding -->
          <div class="shrink-0 mr-4">
            <!-- Logo -->
            <Logo />
          </div>
        </div>
      </div>
    </header>

    <main class="grow">
      <section class="relative">
        <!-- Illustration -->
        <div
          class="hidden md:block absolute left-1/2 -translate-x-1/2 pointer-events-none -z-10"
          aria-hidden="true"
        >
          <img
            src="../images/auth-illustration.svg"
            class="max-w-none"
            width="1440"
            height="332"
            alt="Page Illustration"
          />
        </div>

        <div class="relative max-w-6xl mx-auto px-4 sm:px-6">
          <div class="pt-32 pb-12 md:pt-40 md:pb-20">
            <!-- Page header -->
            <div class="max-w-3xl mx-auto text-center pb-12">
              <h1 class="h2 font-hkgrotesk">Change your password</h1>
            </div>

            <!-- Form -->
            <div class="max-w-sm mx-auto">
              <form>
                <div class="space-y-4">
                  <div>
                    <label
                      class="block text-sm text-slate-500 font-medium mb-1"
                      for="email"
                      >Email</label
                    >
                    <input
                      id="email"
                      class="form-input text-sm py-2 w-full"
                      type="email"
                      required
                    />
                  </div>
                </div>
                <div class="mt-6">
                  <button
                    class="btn-sm text-sm text-white bg-indigo-500 hover:bg-indigo-600 w-full shadow-xs group"
                  >
                    Reset Password
                    <span
                      class="tracking-normal text-sky-300 group-hover:translate-x-0.5 transition-transform duration-150 ease-in-out ml-1"
                      >-&gt;</span
                    >
                  </button>
                </div>
              </form>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  name: "PasswordReset",
  components: {
    Logo,
  },
};

import Logo from "../partials/Logo.vue";
</script>
