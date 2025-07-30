<template>
  <div class="flex flex-col min-h-screen overflow-hidden">
    <!-- Site header -->
    <header class="absolute w-full z-30">
      <div class="max-w-6xl mx-auto px-4 sm:px-6">
        <div class="flex items-center justify-between h-16 md:h-20">
          <!-- Site branding -->
          <div class="shrink-0 mr-4">
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
            <div class="lg:flex lg:space-x-20">
              <!-- Left side -->
              <div
                class="grow lg:mt-20 mb-12 lg:mb-0 flex flex-col items-center lg:items-start"
              >
                <h1 class="h3 font-hkgrotesk mb-8 text-center lg:text-left">
                  Plan smarter. Get more done with AI-powered productivity
                  tools.
                </h1>
                <ul
                  class="inline-flex flex-col text-lg text-slate-500 space-y-3"
                >
                  <li class="flex items-center">
                    <svg
                      class="w-3 h-3 fill-current text-emerald-500 mr-3 shrink-0"
                      viewBox="0 0 12 12"
                    >
                      <path
                        d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z"
                      />
                    </svg>
                    <span>Plan tasks visually and execute with clarity</span>
                  </li>
                  <li class="flex items-center">
                    <svg
                      class="w-3 h-3 fill-current text-emerald-500 mr-3 shrink-0"
                      viewBox="0 0 12 12"
                    >
                      <path
                        d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z"
                      />
                    </svg>
                    <span>Get AI-powered recommendations on the go</span>
                  </li>
                  <li class="flex items-center">
                    <svg
                      class="w-3 h-3 fill-current text-emerald-500 mr-3 shrink-0"
                      viewBox="0 0 12 12"
                    >
                      <path
                        d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z"
                      />
                    </svg>
                    <span>Collaborate seamlessly with clients or teams</span>
                  </li>
                </ul>
              </div>

              <!-- Right side -->
              <div class="relative w-full max-w-md mx-auto">
                <!-- Background gradient -->
                <div
                  class="absolute inset-0 opacity-40 bg-linear-to-t from-transparent to-slate-800 -z-10"
                  aria-hidden="true"
                ></div>

                <div
                  class="p-6 md:p-8 border border-slate-700 rounded-xl bg-slate-800/50"
                >
                  <!-- Coming soon label -->
                  <div class="mb-4 text-center">
                    <span
                      class="inline-block bg-amber-400 text-slate-900 text-xs font-semibold px-3 py-1 rounded-full uppercase tracking-wide"
                    >
                      Coming Soon
                    </span>
                    <p class="text-slate-400 mt-2 text-sm">
                      This feature will be available soon. Stay tuned!
                    </p>
                  </div>

                  <!-- Form -->
                  <form @submit.prevent>
                    <div class="space-y-4">
                      <div class="space-y-4 sm:flex sm:space-y-0 sm:space-x-4">
                        <div class="sm:w-1/2">
                          <label
                            class="block text-sm text-slate-400 font-medium mb-1"
                            for="name"
                            >Name <span class="text-rose-500">*</span></label
                          >
                          <input
                            id="name"
                            class="form-input text-sm py-2 w-full bg-slate-700 border-slate-600"
                            type="text"
                            disabled
                          />
                        </div>
                        <div class="sm:w-1/2">
                          <label
                            class="block text-sm text-slate-400 font-medium mb-1"
                            for="surname"
                            >Surname <span class="text-rose-500">*</span></label
                          >
                          <input
                            id="surname"
                            class="form-input text-sm py-2 w-full bg-slate-700 border-slate-600"
                            type="text"
                            disabled
                          />
                        </div>
                      </div>
                      <div>
                        <label
                          class="block text-sm text-slate-400 font-medium mb-1"
                          for="email"
                          >Email <span class="text-rose-500">*</span></label
                        >
                        <input
                          id="email"
                          class="form-input text-sm py-2 w-full bg-slate-700 border-slate-600"
                          type="email"
                          disabled
                        />
                      </div>
                      <div>
                        <label
                          class="block text-sm text-slate-400 font-medium mb-1"
                          for="phone"
                          >Phone <span class="text-rose-500">*</span></label
                        >
                        <input
                          id="phone"
                          class="form-input text-sm py-2 w-full bg-slate-700 border-slate-600"
                          type="text"
                          disabled
                        />
                      </div>
                      <div>
                        <label
                          class="block text-sm text-slate-400 font-medium mb-1"
                          for="referrer"
                          >How did you hear about us?
                          <span class="text-rose-500">*</span></label
                        >
                        <select
                          id="referrer"
                          class="form-select py-2 w-full bg-slate-700 border-slate-600"
                          disabled
                        >
                          <option>Google</option>
                          <option>Twitter</option>
                          <option>LinkedIn</option>
                          <option>Word of mouth</option>
                        </select>
                      </div>
                      <div>
                        <label
                          class="block text-sm text-slate-400 font-medium mb-1"
                          for="message"
                          >How can we help with?
                          <span class="text-rose-500">*</span></label
                        >
                        <textarea
                          id="message"
                          class="form-textarea text-sm py-2 w-full bg-slate-700 border-slate-600"
                          rows="4"
                          disabled
                        ></textarea>
                      </div>
                    </div>
                    <div class="mt-6">
                      <button
                        class="btn-sm text-sm text-white bg-slate-600 cursor-not-allowed w-full shadow-xs"
                        disabled
                      >
                        Coming Soon
                      </button>
                    </div>
                  </form>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
import Logo from "../partials/Logo.vue";

export default {
  name: "SignIn",
  components: {
    Logo,
  },
};
</script>
