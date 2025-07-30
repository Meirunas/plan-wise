<template>
  <section>
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20 border-b border-slate-800">
        <div class="max-w-sm mx-auto grid gap-8 md:grid-cols-3 lg:gap-16 items-start md:max-w-none">
          <article
            v-for="(testimonial, index) in testimonials"
            :key="index"
            class="h-full flex flex-col items-center text-center"
            :data-aos="'fade-up'"
            :data-aos-delay="index * 200"
          >
            <header class="mb-3">
              <img class="rounded-full inline-flex" :src="testimonial.image" width="40" height="40" :alt="testimonial.alt" />
              <div class="mt-4 flex space-x-1">
                <svg v-for="i in 5" :key="i" class="w-4 h-4 fill-amber-400" viewBox="0 0 16 16">
                  <path d="M10 5.934L8 0 6 5.934H0l4.89 3.954L2.968 16 8 12.223 13.032 16 11.11 9.888 16 5.934z" />
                </svg>
              </div>
            </header>
            <div class="grow mb-3">
              <p class="text-slate-500 italic">"{{ testimonial.quote }}"</p>
            </div>
            <footer class="text-sm text-slate-500 font-medium">
              <a class="text-slate-300 hover:text-white transition duration-150 ease-in-out" href="#0">{{ testimonial.source }}</a>
              - <span class="text-indigo-500">{{ testimonial.rating }}</span>
            </footer>
          </article>

        </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Testimonials',
  data() {
    return {
      testimonials: [
        {
          image: "src/images/testimonial-01.jpg",
          alt: 'Testimonial 01',
          quote: 'PlanWise transformed the way our team organizes tasks - simple, fast, and reliable!',
          source: 'Trustpilot',
          rating: '4.9/5',
        },
        {
          image: 'src/images/testimonial-02.jpg',
          alt: 'Testimonial 02',
          quote: 'An essential tool that keeps our remote team in sync and on target every day.',
          source: 'Capterra',
          rating: '4.7/5',
        },
        {
          image: 'src/images/testimonial-03.jpg',
          alt: 'Testimonial 03',
          quote: 'Saves hours every week powerful and perfectly designed for our workflows.',
          source: 'G2',
          rating: '5/5',
        },
      ],
    }
  },
}
</script>
