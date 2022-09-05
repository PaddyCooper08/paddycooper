<template>
  <div class="h-[1vh] bg-[#122738] text-center">
    <h1 id="typewriter" class="p-5 text-5xl text-[#ffc600]"></h1>
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
      <div class="py-6">
        <div class="flex w-full items-center">
          <h5 class="float-left text-left px-5 text-2xl text-[#ff0088]">
            ~ paddy@cooper/info/about ->
          </h5>
          <h5 class="pl-5 pr-10 text-left text-xl text-[#ffc600]">
            <p id="about"></p>
            <p>
              <a href="/about" class="underline">localhost:3000/about</a>
            </p>
          </h5>
          <!-- <button
            type="button"
            class="
              float-left
              inline-block
              rounded
              border-2 border-[#ffc600]
              px-10
              py-2.5
              text-xs
              font-medium
              uppercase
              leading-tight
              text-[#ff0088]
              transition
              duration-150
              ease-in-out
              hover:bg-black hover:bg-opacity-5
              focus:outline-none focus:ring-0
            "
          >
            Enter
          </button> -->
        </div>
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
    var aboutTypewriter = new Typewriter("#about", {
      autoStart: true,
    });
    aboutTypewriter.pasteString("cat ./about.link ").start();
  },
};
</script>

