<template>
  <div class="h-[1vh] bg-[#122738] text-center">
    <h1 id="typewriter" class="p-5 text-5xl text-[#f7768e]"></h1>
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

<style >
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

* {
  font-family: "Poppins", sans-serif;
}
</style>