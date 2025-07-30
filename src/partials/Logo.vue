<template>
  <router-link
    class="flex items-center space-x-1 group"
    to="/"
    aria-label="PlanWise"
  >
    <svg
      class="w-10 h-10 text-indigo-500 transition-transform duration-200 group-hover:scale-105"
      viewBox="0 0 32 32"
      xmlns="http://www.w3.org/2000/svg"
      role="img"
      aria-hidden="true"
    >
      <title>PlanWise Logo</title>

      <polygon
        points="12.12,2.93 19.88,2.93 26.07,9.12 26.07,16.88 19.88,23.07 12.12,23.07 5.93,16.88 5.93,9.12"
        fill="none"
        stroke="currentColor"
        stroke-width="2.5"
        stroke-linejoin="round"
      />
      <path
        d="M11.5 13.5 L15 17 L21 10.5"
        fill="none"
        stroke="currentColor"
        stroke-width="2.3"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </svg>

    <span
      class="text-base font-semibold tracking-wide text-indigo-500 group-hover:text-indigo-500"
    >
      PLANWISE
    </span>
  </router-link>
</template>

<script>
export default {
  name: "Logo",
};
</script>
