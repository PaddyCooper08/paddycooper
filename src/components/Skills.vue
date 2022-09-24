<template>
  <div class="bg-[#24283b]">
    <!-- Create 3*3 tailwind grid -->

    <div class="flex items-center justify-center float-right mr-[5%] h-screen">
      <div
        class="flex items-center justify-center w-[45%] ml-20 text-center"
        data-aos="fade-right"
        data-aos-duration="2000"
      >
        <h1 class="text-[#f7768e]">Web Dev</h1>
      </div>
      <div
        class="grid grid-cols-3 grid-rows-3 gap-4 items-center w-[50%]"
        data-aos="fade-left"
        data-aos-duration="2000"
      >
        <!-- Loop through skills array -->
        <div
          v-for="skill in skills"
          :key="skill.id"
          class="flex flex-col items-center"
        >
          <!-- Tailwind classes for styling -->
          <img
            :src="skill.image"
            :alt="skill.alt"
            class="w-24 h-24 p-2 rounded-md mb-2 bg-[#343b58]"
          />
          <h3 class="text-xl font-bold text-[#f7768e]">{{ skill.title }}</h3>
          <p class="text-[#bb9af7] text-center">{{ skill.description }}</p>
        </div>
      </div>
    </div>
    <div
      data-aos="fade-right"
      data-aos-duration="2000"
      class="w-[50%] flex items-center justify-center ml-[5%] h-screen"
    >
      <div class="grid grid-cols-3 grid-rows-3 gap-4 items-center">
        <!-- Loop through skills array -->
        <div
          v-for="skill in skills"
          :key="skill.id"
          class="flex flex-col items-center"
        >
          <!-- Tailwind classes for styling -->
          <img
            :src="skill.image"
            :alt="skill.alt"
            class="w-24 h-24 p-2 rounded-md mb-2 bg-[#343b58]"
          />
          <h3 class="text-xl font-bold text-[#f7768e]">{{ skill.title }}</h3>
          <p class="text-[#bb9af7] text-center">{{ skill.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css"; // You can also use <link> for styles
export default {
  mounted() {
    AOS.init();
  },
  // data is a function that returns an object
  data() {
    return {
      // Array of skills
      skills: [
        {
          id: 1,
          title: "HTML",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg",
          alt: "HTML",
        },
        {
          id: 2,
          title: "CSS",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg",
          alt: "CSS",
        },

        {
          id: 3,
          title: "JavaScript",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
          alt: "JavaScript",
        },
        {
          id: 4,
          title: "Vue",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg",
          alt: "Vue",
        },
        {
          id: 5,
          title: "Astro",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/astro.build/assets/press/logomark-dark.svg",
          alt: "Astro",
        },

        {
          id: 6,
          title: "Tailwind",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg",
          alt: "Tailwind",
        },

        {
          id: 7,
          title: "Github",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg",
          alt: "Github",
        },
        {
          id: 8,
          title: "Vercel",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/gh/PaddyCooper08/portfolio/dee845fa/images/vercel.svg",
          alt: "Vercel",
        },
        {
          id: 9,
          title: "Django",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg",
          alt: "Django",
        },
      ],
    };
  },
};
</script>

<style></style>
