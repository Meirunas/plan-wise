<template>
  <section class="relative">
    <!-- Illustration -->
    <div
      class="hidden lg:block absolute bottom-0 left-1/2 -translate-x-1/2 -mb-24 pointer-events-none -z-10"
      aria-hidden="true"
    >
      <img
        src="../images/pricing-illustration.svg"
        class="max-w-none"
        width="1440"
        height="440"
        alt="Pricing Illustration"
      />
    </div>

    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="pt-10 pb-12 md:pb-20">
        <!-- Section header -->
        <div class="max-w-3xl mx-auto text-center pb-12 md:pb-20">
          <h2 class="h2 font-hkgrotesk mb-4">
            Choose the right plan to boost your productivity
          </h2>
          <p class="text-xl text-slate-500">
            PlanWise Pro gives you everything you need to manage teams, tasks
            and progress - whether you're solo or growing fast.
          </p>
        </div>

        <!-- Pricing tables -->
        <div class="grid md:grid-cols-6">
          <!-- Pricing toggle -->
          <div
            class="flex flex-col justify-center p-4 md:px-6 bg-slate-800 md:col-span-3"
          >
            <div
              class="flex justify-center md:justify-start items-center space-x-4"
            >
              <div
                class="text-sm text-slate-500 font-medium min-w-[6rem] md:min-w-0 text-right"
              >
                Monthly
              </div>
              <div class="form-switch shrink-0">
                <input
                  type="checkbox"
                  id="toggle"
                  class="sr-only"
                  v-model="annual"
                />
                <label class="bg-slate-900" for="toggle">
                  <span aria-hidden="true"></span>
                  <span class="sr-only">Pay annually</span>
                </label>
              </div>
              <div class="text-sm text-slate-500 font-medium min-w-[6rem]">
                Yearly <span class="text-emerald-500">(-20%)</span>
              </div>
            </div>
          </div>

          <!-- Plan cards -->
          <div
            v-for="(plan, index) in plans"
            :key="plan.name"
            :class="`flex flex-col justify-center p-4 md:px-6 bg-slate-800 md:border-l border-slate-700 md:text-center mt-6 md:mt-0 order-${
              index + 1
            } md:order-none`"
          >
            <div
              class="font-hkgrotesk text-lg font-bold text-indigo-500 mb-0.5"
            >
              {{ plan.name }}
            </div>
            <div>
              <span class="text-xl font-semibold">£</span>
              <span class="text-2xl font-semibold">
                {{ annual ? plan.annual : plan.monthly }}
              </span>
              <span class="text-sm text-slate-500 font-medium">/mo</span>
            </div>
          </div>

          <!-- Looping label and feature rows -->
          <template v-for="(row, rowIndex) in featureRows" :key="rowIndex">
            <!-- Label Row -->
            <div
              v-if="row.label"
              class="hidden md:flex flex-col justify-center px-4 md:px-6 py-2 bg-slate-700/25 md:col-span-3"
            >
              <span class="text-xs uppercase font-semibold text-slate-500">
                {{ row.label }}
              </span>
            </div>
            <div
              v-for="(col, colIndex) in row.values"
              :key="`col-${rowIndex}-${colIndex}`"
              :class="[
                'flex flex-col justify-center px-4 md:px-6 py-2 bg-slate-700/25 md:border-l border-slate-700',
                `order-${colIndex + 1} md:order-none`,
              ]"
            >
              <span
                class="md:hidden text-xs uppercase font-semibold text-slate-500"
              >
                {{ row.label }}
              </span>
            </div>

            <!-- Feature Row -->
            <div
              v-if="row.name"
              :class="[
                'hidden md:flex flex-col justify-center p-4 md:px-6 md:col-span-3',
                row.alt ? 'bg-slate-800/70' : 'bg-slate-800',
              ]"
            >
              <div class="text-slate-200">{{ row.name }}</div>
            </div>
            <div
              v-for="(value, colIndex) in row.data"
              :key="`val-${rowIndex}-${colIndex}`"
              :class="[
                'flex justify-between md:flex-col md:justify-center p-4 md:px-6',
                row.alt ? 'bg-slate-800/70' : 'bg-slate-800',
                'md:border-l border-slate-700',
                `order-${colIndex + 1} md:order-none`,
              ]"
            >
              <div class="md:hidden text-slate-200">{{ row.name }}</div>
              <div
                class="text-sm font-medium text-slate-200 text-center"
                v-html="value"
              ></div>
            </div>
          </template>

          <!-- CTA row -->
          <div
            class="hidden md:flex flex-col justify-center px-4 md:px-6 py-2 bg-slate-700/25 md:col-span-3"
          ></div>

          <div
            v-for="(plan, index) in plans"
            :key="`cta-${index}`"
            :class="`flex flex-col justify-center p-4 bg-slate-700/25 md:border-l border-slate-700 order-${
              index + 1
            } md:order-none`"
          >
            <div v-if="annual" class="text-sm text-slate-400 text-center">
              Coming Soon
            </div>
            <a
              v-else
              class="btn-sm text-white bg-indigo-500 hover:bg-indigo-600 w-full shadow-xs group whitespace-nowrap text-center"
              :href="plan.link"
            >
              Free Trial
              <span
                class="hidden lg:block tracking-normal text-sky-300 group-hover:translate-x-0.5 transition-transform duration-150 ease-in-out ml-1"
              >
                -&gt;
              </span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ref } from "vue";

export default {
  name: "Pricing",
  setup() {
    const annual = ref(false);

    const plans = [
      { name: "Starter", monthly: "25", annual: "20", link: "#starter-link" },
      { name: "Agency", monthly: "45", annual: "36", link: "#agency-link" },
      { name: "Team", monthly: "70", annual: "55", link: "#team-link" },
    ];

    const checkIcon =
      '<svg class="inline-flex fill-emerald-400" width="12" height="9" xmlns="http://www.w3.org/2000/svg"><path d="M10.28.28 3.989 6.575 1.695 4.28A1 1 0 0 0 .28 5.695l3 3a1 1 0 0 0 1.414 0l7-7A1 1 0 0 0 10.28.28Z" fill="#34D399" fill-rule="nonzero" /></svg>';
    const dashIcon =
      '<svg class="inline-flex fill-slate-500" width="14" height="2" xmlns="http://www.w3.org/2000/svg"><path d="M14 0v2H0V0z" fill-rule="evenodd" /></svg>';

    const featureRows = [
      { label: "Usage", values: [1, 2, 3] },
      { name: "Admins & Members", data: ["4", "12", "Unlimited"] },
      { name: "File Storage", data: ["10GB", "50GB", "Unlimited"], alt: true },
      { name: "Active Users", data: ["500", "1500", "Unlimited"] },
      { label: "Features", values: [1, 2, 3] },
      { name: "Unlimited Activities", data: [checkIcon, checkIcon, checkIcon] },
      {
        name: "Data Export",
        data: [dashIcon, checkIcon, checkIcon],
        alt: true,
      },
      { name: "Adjust Group Sizes", data: [dashIcon, checkIcon, checkIcon] },
    ];

    return {
      annual,
      plans,
      featureRows,
    };
  },
};
</script>
