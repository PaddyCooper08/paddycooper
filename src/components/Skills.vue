<template>
  <div class="bg-[#24283b] h-[100vh]">
    <!-- Create 3*3 tailwind grid -->
    <div class="w-[50%] h-full">
      <div class="grid grid-cols-3 grid-rows-3 gap-4">
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
          <h3 class="text-xl font-bold">{{ skill.title }}</h3>
          <p class="text-gray-500">{{ skill.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
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
          title: "Tailwind",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg",
          alt: "Tailwind",
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
          title: "Astro",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://astro.build/assets/press/logomark-dark.svg",
          alt: "Astro",
        },
        {
          id: 5,
          title: "Vue",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg",
          alt: "Vue",
        },
        {
          id: 6,
          title: "CSS",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg",
          alt: "CSS",
        },
        {
          id: 7,
          title: "CSS",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg",
          alt: "CSS",
        },
        {
          id: 8,
          title: "CSS",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg",
          alt: "CSS",
        },
        {
          id: 9,
          title: "CSS",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image: "https://cdn.statically.io/img/:domain/:image",
          alt: "CSS",
        },
      ],
    };
  },
};
</script>

<style>
</style>