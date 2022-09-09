<template>
  <div class="h-[1vh] bg-[#122738] text-center">
    <h1 id="typewriter" class="p-5 text-5xl text-[#ffc600]"></h1>
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

<style>
</style>