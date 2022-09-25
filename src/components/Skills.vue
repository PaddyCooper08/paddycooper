<template>
  <div class="bg-[#24283b]">
    <!-- Create 3*3 tailwind grid -->

    <div class="flex items-center justify-center h-screen">
      <div
        class="flex items-center justify-center w-[45%] ml-20 text-center"
        data-aos="fade-right"
        data-aos-duration="2000"
      >
        <div class="rounded-lg h-[75%] w-[95%] bg-[#343b58] text-center">
          <h1 class="text-3xl text-[#f7768e] mt-[5%]">Frontend Skills</h1>
          <section
            id="splide"
            class="splide"
            aria-label="Splide Basic HTML Example"
          >
            <div id="splide" class="splide__track">
              <ul id="splide" class="splide__list">
                <li id="splide" class="splide__slide text-[#73daca]">
                  Rideshare Website
                  <img
                    src="https://cdn.statically.io/gh/PaddyCooper08/portfolio/f055f637/images/rideshare1.png"
                    alt=""
                    class="h-full w-full"
                  />
                </li>
                <li id="splide" class="splide__slide text-[#73daca]">
                  Rideshare Website
                  <img
                    src="https://cdn.statically.io/gh/PaddyCooper08/portfolio/f055f637/images/rideshare2.svg"
                    alt=""
                    class="h-full w-full"
                  />
                </li>
                <li id="splide" class="splide__slide text-[#73daca]">
                  Rideshare Website
                  <img
                    src="https://cdn.statically.io/gh/PaddyCooper08/portfolio/f055f637/images/rideshare3.png"
                    alt=""
                    class="h-full w-full"
                  />
                </li>
              </ul>
            </div>
          </section>
        </div>
      </div>
      <div
        class="
          grid grid-cols-3 grid-rows-3
          gap-4
          items-center
          w-[50%]
          float-right
          mr-[5%]
        "
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
    <div class="flex items-center justify-center h-screen">
      <div
        class="
          grid grid-cols-3 grid-rows-3
          gap-4
          items-center
          w-[50%]
          float-left
          mr-[5%]
        "
        data-aos="fade-left"
        data-aos-duration="2000"
      >
        <!-- Loop through skills array -->
        <div
          v-for="backend_skill in backend_skills"
          :key="backend_skill.id"
          class="flex flex-col items-center"
        >
          <!-- Tailwind classes for styling -->
          <img
            :src="backend_skill.image"
            :alt="backend_skill.alt"
            class="w-24 h-24 p-2 rounded-md mb-2 bg-[#343b58]"
          />
          <h3 class="text-xl font-bold text-[#f7768e]">
            {{ backend_skill.title }}
          </h3>
          <p class="text-[#bb9af7] text-center">
            {{ backend_skill.description }}
          </p>
        </div>
      </div>
      <div
        class="
          flex
          items-center
          justify-center
          w-[45%]
          mr-20
          text-center
          float-right
        "
        data-aos="fade-right"
        data-aos-duration="2000"
      >
        <div class="rounded-lg h-[75%] w-[95%] bg-[#343b58] text-center">
          <h1 class="text-3xl text-[#f7768e] mt-[4%]">Backend/Python Skills</h1>
          <section id="splide1" class="splide">
            <div id="splide1" class="splide__track">
              <ul id="splide1" class="splide__list">
                <li
                  id="splide1"
                  class="splide__slide text-[#73daca] items-center mx-auto"
                >
                  Simple email server
                  <a href="https://github.com/PaddyCooper08/emailServer"
                    ><img
                      class="mx-auto h-full w-full"
                      src="https://gh-card.dev/repos/PaddyCooper08/emailServer.svg?fullname"
                  /></a>
                </li>
                <li id="splide1" class="splide__slide text-[#73daca]">
                  Discord.py bot
                  <a href="https://github.com/PaddyCooper08/Zygote-bot"
                    ><img
                      class="mx-auto h-full w-full"
                      src="https://gh-card.dev/repos/PaddyCooper08/Zygote-bot.svg?fullname"
                  /></a>
                </li>
                <li id="splide1" class="splide__slide text-[#73daca]">
                  Machine Learning security camera
                  <a href="https://github.com/PaddyCooper08/SecurityCam"
                    ><img
                      class="mx-auto h-full w-full"
                      src="https://gh-card.dev/repos/PaddyCooper08/SecurityCam.svg?fullname="
                  /></a>
                </li>
              </ul>
            </div>
          </section>
        </div>
      </div>
    </div>
    <div class="flex items-center justify-center h-screen">
      <div
        class="flex items-center justify-center w-[45%] ml-20 text-center"
        data-aos="fade-right"
        data-aos-duration="2000"
      >
        <div class="rounded-lg h-[75%] w-[95%] bg-[#343b58] text-center">
          <h1 class="text-3xl text-[#f7768e] mt-[5%]">IRL Skills</h1>
          <section
            id="splide2"
            class="splide"
            aria-label="Splide Basic HTML Example"
          >
            <div id="splide2" class="splide__track">
              <ul id="splide2" class="splide__list">
                <li id="splide2" class="splide__slide text-[#73daca]">
                  <a href="https://pexels.com" target="_blank"
                    >Images from Pexels</a
                  >
                  <img
                    src="https://cdn.statically.io/img/images.pexels.com/photos/1627960/pexels-photo-1627960.jpeg"
                    alt=""
                    class="h-full w-full"
                  />
                </li>
                <li id="splide2" class="splide__slide text-[#73daca]">
                  <a href="https://pexels.com" target="_blank"
                    >Images from Pexels</a
                  >
                  <img
                    src="https://cdn.statically.io/img/images.pexels.com/photos/3599596/pexels-photo-3599596.jpeg"
                    alt=""
                    class="h-full w-full"
                  />
                </li>
                <li id="splide2" class="splide__slide text-[#73daca]">
                  <a href="https://pexels.com" target="_blank"
                    >Images from Pexels</a
                  >
                  <img
                    src="https://cdn.statically.io/img/images.pexels.com/photos/90454/pexels-photo-90454.jpeg"
                    alt=""
                    class="h-full w-full"
                  />
                </li>
              </ul>
            </div>
          </section>
        </div>
      </div>
      <div
        class="
          grid grid-cols-3 grid-rows-3
          gap-4
          items-center
          w-[50%]
          float-right
          mr-[5%]
        "
        data-aos="fade-left"
        data-aos-duration="2000"
      >
        <!-- Loop through skills array -->
        <div
          v-for="irl_skill in irl_skills"
          :key="irl_skill.id"
          class="flex flex-col items-center"
        >
          <!-- Tailwind classes for styling -->
          <img
            :src="irl_skill.image"
            :alt="irl_skill.alt"
            class="w-24 h-24 p-2 rounded-md mb-2 bg-[#343b58]"
          />
          <h3 class="text-xl font-bold text-[#f7768e]">
            {{ irl_skill.title }}
          </h3>
          <p class="text-[#bb9af7] text-center">{{ irl_skill.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css"; // You can also use <link> for styles
import "@splidejs/splide/css";
import Splide from "@splidejs/splide";

export default {
  mounted() {
    AOS.init();
    new Splide("#splide", {
      type: "loop",
      perPage: 1,
      perMove: 1,
      gap: "1rem",
      pagination: false,
      autoplay: true,
      interval: 3000,
      easing: "ease-in-out",
    }).mount();
    new Splide("#splide1", {
      type: "loop",
      perPage: 1,
      perMove: 1,
      gap: "1rem",
      pagination: false,
      autoplay: true,
      interval: 3000,
      easing: "ease-in-out",
    }).mount();
    new Splide("#splide2", {
      type: "loop",
      perPage: 1,
      perMove: 1,
      gap: "1rem",
      pagination: false,
      autoplay: true,
      interval: 3000,
      easing: "ease-in-out",
    }).mount();
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
          title: "Bootstrap",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg",
          alt: "Bootstrap",
        },
      ],
      backend_skills: [
        {
          id: 1,
          title: "NodeJS",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg",
          alt: "NodeJS",
        },
        {
          id: 2,
          title: "NPM",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/npm/npm-original-wordmark.svg",
          alt: "NPM",
        },

        {
          id: 3,
          title: "Express",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg",
          alt: "Express",
        },

        {
          id: 4,
          title: "Python",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg",
          alt: "Python",
        },
        {
          id: 5,
          title: "Django",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg",
          alt: "Django",
        },

        {
          id: 6,
          title: "Flask",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flask/flask-original.svg",
          alt: "Flask",
        },

        {
          id: 7,
          title: "Heroku",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/heroku/heroku-original.svg",
          alt: "Heroku",
        },
        {
          id: 8,
          title: "Docker",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-plain.svg",
          alt: "Docker",
        },
        {
          id: 9,
          title: "Discord.py",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/assets-global.website-files.com/6257adef93867e50d84d30e2/62595384e89d1d54d704ece7_3437c10597c1526c3dbd98c737c2bcae.svg",
          alt: "Discord.py",
        },
      ],
      irl_skills: [
        {
          id: 1,
          title: "Rugby",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/1984/1984764.png",
          alt: "Rugby",
        },
        {
          id: 2,
          title: "Hockey",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/4242/4242218.png",
          alt: "Hockey",
        },

        {
          id: 3,
          title: "Badminton",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/2633/2633871.png",
          alt: "Badminton",
        },

        {
          id: 4,
          title: "Woodworking",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/2716/2716870.png",
          alt: "Woodworking",
        },
        {
          id: 5,
          title: "Mountain Biking",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/1275/1275397.png",
          alt: "Mountain Biking",
        },

        {
          id: 6,
          title: "Focusing",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/3389/3389081.png",
          alt: "Focusing",
        },

        {
          id: 7,
          title: "Reading",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/3145/3145765.png",
          alt: "Reading",
        },
        {
          id: 8,
          title: "Organisation",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/3652/3652191.png",
          alt: "Organisation",
        },
        {
          id: 9,
          title: "Communication",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          image:
            "https://cdn.statically.io/img/cdn-icons-png.flaticon.com/512/3050/3050525.png",
          alt: "Communication",
        },
      ],
    };
  },
};
</script>

<style></style>
