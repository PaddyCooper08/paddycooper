<template>
  <div class="h-[1vh] text-center bg-[#122738]">
    <h1 id="typewriter" class="text-5xl p-5 text-[#ffc600]"></h1>
  </div>
  <div class="flex h-[99vh] items-center justify-center bg-[#122738]">
    <div
      class="
        mx-auto
        my-auto
        h-[80%]
        w-[60%]
        rounded-lg
        bg-[#193549]
        text-center
        shadow-lg
        only:block
      "
    >
      <div
        class="
          border-b-2 border-[#ffc600]
          py-3
          px-6
          text-xl
          font-bold
          text-[#ff0088]
        "
      >
        CMD
      </div>
      <div class="p-6">
        <h5 class="mb-2 text-xl font-medium text-gray-900">
          Special title treatment
        </h5>
        <p class="mb-4 text-base text-gray-700">
          With supporting text below as a natural lead-in to additional content.
        </p>
        <button
          type="button"
          class="
            inline-block
            rounded
            bg-blue-600
            px-6
            py-2.5
            text-xs
            font-medium
            uppercase
            leading-tight
            text-white
            shadow-md
            transition
            duration-150
            ease-in-out
            hover:bg-blue-700 hover:shadow-lg
            focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0
            active:bg-blue-800 active:shadow-lg
          "
        >
          Button
        </button>
      </div>
      <div class="border-t border-gray-300 py-3 px-6 text-gray-600">
        2 days ago
      </div>
    </div>
  </div>
</template>

<script>
import Typewriter from "typewriter-effect/dist/core";
export default {
  mounted() {
    var typewriter = new Typewriter("#typewriter", {
      autoStart: true,
    });
    typewriter
      .typeString(">Paddy Cooper - Developer")
      .pauseFor(450)
      .deleteChars(9)
      .typeString("Problem Solver")
      .pauseFor(450)
      .deleteChars(14)
      .pauseFor(50)
      .typeString("Designer")
      .pauseFor(450)
      .deleteChars(8)
      .pauseFor(50)
      .typeString("Entrepreneur")
      .pauseFor(450)
      .deleteChars(12)
      .typeString("Legend 💪")
      .pauseFor(450)

      .start();
  },
};
</script>

