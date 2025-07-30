<template>
  <section class="relative">
    <!-- Bg illustration -->
    <div
      class="absolute left-1/2 -translate-x-1/2 pointer-events-none -mt-20 -z-10"
      aria-hidden="true"
    >
      <img
        src="../images/features-illustration.svg"
        class="max-w-none"
        width="1440"
        height="440"
        alt="Illustration"
      />
    </div>

    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20">
        <!-- Section header -->
        <div class="max-w-3xl mx-auto text-center pb-12 md:pb-20">
          <h2 class="h2 font-hkgrotesk mb-4">
            Many tools to express your creativity
          </h2>
          <div class="max-w-2xl mx-auto">
            <p class="text-xl text-slate-500">
              Discover smart features designed to empower your workflow and
              boost productivity.
            </p>
          </div>
        </div>

        <!-- Carousel -->
        <div class="swiper carousel">
          <div class="swiper-wrapper">
            <div
              class="swiper-slide flex flex-col items-center text-center bg-slate-800 p-6 rounded-xl"
              v-for="(feature, index) in features"
              :key="index"
            >
              <img
                :src="feature.icon"
                width="56"
                height="56"
                :alt="feature.alt"
                class="mb-4"
              />
              <h3 class="text-xl font-bold text-white mb-2">
                {{ feature.title }}
              </h3>
              <p class="text-slate-400">{{ feature.description }}</p>
            </div>
          </div>

          <!-- Arrows -->
          <div class="flex mt-12 space-x-4 justify-center">
            <button
              class="carousel-prev w-12 h-12 rounded-full flex items-center justify-center border border-slate-700 bg-slate-800 hover:bg-slate-700"
            >
              <svg
                class="w-4 h-4 fill-slate-400"
                viewBox="0 0 16 16"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M6.7 14.7l1.4-1.4L3.8 9H16V7H3.8l4.3-4.3-1.4-1.4L0 8z"
                />
              </svg>
            </button>
            <button
              class="carousel-next w-12 h-12 rounded-full flex items-center justify-center border border-slate-700 bg-slate-800 hover:bg-slate-700"
            >
              <svg
                class="w-4 h-4 fill-slate-400"
                viewBox="0 0 16 16"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M9.3 14.7l-1.4-1.4L12.2 9H0V7h12.2L7.9 2.7l1.4-1.4L16 8z"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Swiper, { Autoplay, Navigation } from "swiper";
import "swiper/css";
Swiper.use([Autoplay, Navigation]);

export default {
  name: "Features",
  data() {
    return {
      features: [
        {
          title: "Collaboration",
          description:
            "Collaborate effortlessly in real-time and stay aligned with your team’s goals.",
          icon: "src/images/features-icon-01.svg",
          alt: "Collaboration",
        },
        {
          title: "Experiences",
          description:
            "Customize your workspace with flexible layouts and smooth workflows.",
          icon: "src/images/features-icon-02.svg",
          alt: "Experiences",
        },
        {
          title: "Animation",
          description:
            "Animate your ideas with motion-based visuals and interactive timelines.",
          icon: "src/images/features-icon-03.svg",
          alt: "Animation",
        },
        {
          title: "Modeling",
          description:
            "Visualize and refine ideas with interactive dashboards and real-time insights.",
          icon: "src/images/features-icon-04.svg",
          alt: "Modeling",
        },
      ],
    };
  },
  mounted() {
    new Swiper(".carousel", {
      loop: true,
      grabCursor: true,
      spaceBetween: 24,
      autoplay: {
        delay: 3000,
        disableOnInteraction: false,
      },
      navigation: {
        nextEl: ".carousel-next",
        prevEl: ".carousel-prev",
      },
      breakpoints: {
        320: { slidesPerView: 1 },
        768: { slidesPerView: 2 },
        1024: { slidesPerView: 3 },
      },
    });
  },
};
</script>
