<template>
  <section class="relative border-t border-slate-800">
    <!-- Bg gradient -->
    <div
      class="absolute top-0 left-0 right-0 h-[25rem] bg-gradient-to-b from-slate-800 to-transparent opacity-25 pointer-events-none -z-10"
      aria-hidden="true"
    ></div>

    <!-- Illustration background image -->
    <div
      class="hidden lg:block absolute top-0 left-1/2 -translate-x-1/2 mt-40 pointer-events-none -z-10"
      aria-hidden="true"
    >
      <img
        src="../images/features-illustration-02.svg"
        class="max-w-none"
        width="1440"
        height="453"
        alt="Background Illustration"
      />
    </div>

    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20">
        <!-- Section header -->
        <div class="max-w-3xl mx-auto text-center pb-12 md:pb-20">
          <h2 class="h2 font-hkgrotesk">
            Features to help you create your best
          </h2>
        </div>

        <!-- Box -->
        <div class="bg-slate-800/60 rounded-sm overflow-hidden">
          <div
            class="flex flex-col md:flex-row items-end md:items-start md:justify-between lg:space-x-20"
          >
            <!-- Text and filters -->
            <div class="md:min-w-[28rem] p-6 lg:p-10">
              <!-- Category filters -->
              <div class="mb-6 lg:mb-8">
                <div class="flex flex-wrap -m-1.5">
                  <button
                    v-for="item in features"
                    :key="item.id"
                    class="btn-sm px-3 py-1 shadow-xs rounded-full m-1.5"
                    :class="
                      category === item.id
                        ? 'text-white bg-indigo-500'
                        : 'text-slate-300 bg-slate-700 hover:bg-slate-600 border-slate-600'
                    "
                    @click="category = item.id"
                  >
                    {{ item.name }}
                  </button>
                </div>
              </div>

              <!-- Dynamic content -->
              <div
                v-for="item in features"
                :key="item.id"
                v-show="category === item.id"
              >
                <h3 class="h3 font-hkgrotesk mb-2">{{ item.title }}</h3>
                <div class="text-lg text-slate-500">{{ item.description }}</div>
              </div>
            </div>

            <!-- Illustration image -->
            <img
              src="../images/features-image.png"
              class="md:max-w-none"
              width="480"
              height="414"
              alt="Feature Image"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "FeatureGroups",
  data() {
    return {
      category: "1",
      features: [
        {
          id: "1",
          name: "Everyone",
          title: "Kickstart your project with powerful AI tools",
          description:
            "From goal setting to task completion, PlanWise gives everyone a head start. Smart suggestions, clean design and intuitive tools mean you can stay focused and productive whether you're planning a trip or building your dream app.",
        },
        {
          id: "2",
          name: "Freelancers",
          title: "Stay organised and impress clients effortlessly",
          description:
            "PlanWise is your all-in-one dashboard for managing projects, tracking milestones and communicating clearly. Freelancers love how it helps them juggle multiple clients, deliver faster and build long-term trust with clean, professional plans.",
        },
        {
          id: "3",
          name: "Organisations",
          title: "Align teams and scale smarter with shared vision",
          description:
            "Whether you're a startup or a growing company, PlanWise helps your team align around shared goals. Visual planning, automation and real-time updates let you reduce risk, move faster and execute more efficiently together.",
        },
      ],
    };
  },
};
</script>
