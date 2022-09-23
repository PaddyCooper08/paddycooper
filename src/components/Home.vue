<template>
  <div class="flex h-[99vh] items-center justify-center bg-[#24283b]">
    <div
      class="
        mx-auto
        my-auto
        h-[80%]
        w-[60%]
        rounded-lg
        bg-[#a9b1d6]
        text-center
        shadow-lg
        only:block
      "
    >
      <div
        class="
          border-b-2 border-[ #a9b1d6]
          py-3
          px-6
          text-xl
          font-bold
          text-[#73daca]
        "
      >
        CMD
      </div>
      <div class="py-6">
        <div class="flex w-full items-center">
          <h5 class="float-left text-left px-5 text-2xl text-[#73daca]">
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
</script>

<style >
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

* {
  font-family: "Poppins", sans-serif;
}
</style>
