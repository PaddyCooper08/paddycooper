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
      .typeString(">About")

      .start();
  },
};
</script>

<style>
</style>