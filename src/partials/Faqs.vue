<template>
  <section>
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20">
        <!-- Section header -->
        <div class="pb-12 md:pb-20 text-center">
          <h2 class="text-3xl md:text-4xl font-bold font-hkgrotesk">
            Frequently Asked Questions
          </h2>
          <p class="mt-4 text-slate-500 text-base md:text-lg">
            Answers to common questions about our product and services.
          </p>
        </div>

        <!-- Two Columns -->
        <div class="md:flex md:space-x-12 space-y-8 md:space-y-0">
          <!-- Left Column -->
          <div class="w-full md:w-1/2 space-y-8">
            <div
              v-for="(item, index) in faqs.slice(0, Math.ceil(faqs.length / 2))"
              :key="'left-' + index"
              class="space-y-2"
            >
              <h4 class="text-xl font-semibold font-hkgrotesk">
                {{ item.question }}
              </h4>
              <p class="text-slate-500">
                {{ item.answer }}
              </p>
            </div>
          </div>

          <!-- Right Column -->
          <div class="w-full md:w-1/2 space-y-8">
            <div
              v-for="(item, index) in faqs.slice(Math.ceil(faqs.length / 2))"
              :key="'right-' + index"
              class="space-y-2"
            >
              <h4 class="text-xl font-semibold font-hkgrotesk">
                {{ item.question }}
              </h4>
              <p class="text-slate-500">
                {{ item.answer }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Faqs",
  data() {
    return {
      faqs: [
        {
          question: "What's the difference between Free and Paid versions?",
          answer:
            "The Free version includes core features with limited usage, ideal for individuals. The Paid version offers advanced features, more integrations, and priority support - perfect for teams and businesses.",
        },
        {
          question: "Do you offer student or non-profit discounts?",
          answer:
            "Yes! We support students and registered non-profits with a 30% discount. Contact our support team with proof of eligibility to receive the offer.",
        },
        {
          question: "How is pricing calculated?",
          answer:
            "Pricing is based on the number of users and the level of features needed. We offer monthly and yearly billing with savings on annual plans.",
        },
        {
          question: "Do I need coding knowledge to use this product?",
          answer:
            "No coding required! Our platform is built for non-technical users with an intuitive drag-and-drop interface and smart AI-powered tools.",
        },
        {
          question: "Can I join your Affiliate Program?",
          answer:
            "Yes! We welcome content creators, educators, and businesses to earn commission through referrals. Sign up through our Affiliate Portal.",
        },
        {
          question: "What payment methods are supported?",
          answer:
            "We accept major credit and debit cards, PayPal and international transfers for annual plans. Invoices are also available for enterprise customers.",
        },
      ],
    };
  },
};
</script>
