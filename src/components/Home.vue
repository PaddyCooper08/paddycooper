<template>
  <div id="tiles"></div>

  <h1 id="title" class="centered">
    <span class="magic" v-show="showName">
      <span class="magic-star">
        <svg viewBox="0 0 512 512">
          <path
            d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z"
          />
        </svg>
      </span>
      <span class="magic-star">
        <svg viewBox="0 0 512 512">
          <path
            d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z"
          />
        </svg>
      </span>
      <span class="magic-star">
        <svg viewBox="0 0 512 512">
          <path
            d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z"
          />
        </svg>
      </span>
      <span id="typewriter" class="magic-text">Paddy Cooper</span>
    </span>
  </h1>

  <div id="boom"></div>
</template>

<script>
import Typewriter from "typewriter-effect/dist/core";

export default {
  data() {
    return {
      showName: true,
    };
  },
  mounted() {
    var h = document.getElementsByTagName("head").item(0);
    const wrapper = document.getElementById("tiles");
    var s = document.createElement("script");
    s.src = "https://cdnjs.cloudflare.com/ajax/libs/animejs/3.2.1/anime.min.js";
    h.appendChild(s);
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

    let columns = 0,
      rows = 0,
      toggled = false;
    function getOffset(el) {
      const rect = el.getBoundingClientRect();
      return {
        left: Math.round(rect.x),
        top: Math.round(rect.y),
      };
    }

    const toggle = () => {
      toggled = !toggled;
      this.showName = !this.showName;
      if (this.showName) {
        typewriter.start();
      } else {
        typewriter.pause();
      }
      document.body.classList.remove("break");
      let boom = document.getElementById("boom");
      boom.classList.remove("animate");

      document.body.classList.toggle("toggled");
    };

    const handleOnClick = (index) => {
      toggle();

      anime({
        targets: ".tile",
        opacity: toggled ? 0 : 1,
        delay: anime.stagger(50, {
          grid: [columns, rows],
          from: index,
        }),
      });
    };

    const createTile = (index) => {
      const tile = document.createElement("div");

      tile.classList.add("tile");
      tile.setAttribute("id", index);

      tile.style.opacity = toggled ? 0 : 1;

      tile.onclick = (e) => {
        handleOnClick(index);
      };
      tile.ondblclick = (e) => {
        if (!toggled) {
          let el = document.getElementById(index);
          console.log(getOffset(el));
          var r = document.querySelector(":root");
          r.style.setProperty("--top", getOffset(el).top + "px");
          r.style.setProperty("--left", getOffset(el).left + "px");
          r.style.setProperty("--visible", 1);
          let boom = document.getElementById("boom");
          boom.setAttribute("class", "animate");
          let b = document.querySelector("body");
          b.setAttribute("class", "break");
        }
      };

      return tile;
    };

    const createTiles = (quantity) => {
      Array.from(Array(quantity)).map((tile, index) => {
        wrapper.appendChild(createTile(index));
      });
    };

    const createGrid = () => {
      wrapper.innerHTML = "";

      const size = document.body.clientWidth > 800 ? 100 : 50;

      columns = Math.floor(document.body.clientWidth / size);
      rows = Math.floor(document.body.clientHeight / size);

      wrapper.style.setProperty("--columns", columns);
      wrapper.style.setProperty("--rows", rows);

      createTiles(columns * rows);
    };

    createGrid();

    window.onresize = () => createGrid();
    let index = 0,
      interval = 1000;

    const rand = (min, max) =>
      Math.floor(Math.random() * (max - min + 1)) + min;

    const animate = (star) => {
      star.style.setProperty("--star-left", `${rand(-10, 100)}%`);
      star.style.setProperty("--star-top", `${rand(-40, 80)}%`);

      star.style.animation = "none";
      star.offsetHeight;
      star.style.animation = "";
    };

    for (const star of document.getElementsByClassName("magic-star")) {
      setTimeout(() => {
        animate(star);

        setInterval(() => animate(star), 1000);
      }, index++ * (interval / 3));
    }
  },
};
</script>

<style>
:root {
  --g1: #f7768e;
  --g2: #bb9af7;
  --top: 0%
  --left: 0%
  --visible: 0;
  --blue: rgb(115, 218, 202);
  --violet: rgb(187, 154, 247);
  --pink: rgb(247, 118, 142);
}

@keyframes background-pan {
  from {
    background-position: 0% center;
  }

  to {
    background-position: -200% center;
  }
}
.break {
  animation: break 6s ease-in-out forwards;
}
body {
  animation: background-pan 10s linear infinite;
  background: linear-gradient(to right, var(--g1), var(--g2), var(--g1));
  background-size: 200%;
  height: 100vh;
  overflow: hidden;
  margin: 0px;
}

body.toggled {
  animation: none;
  background: none;
  background-color: #343b58;

}


body.toggled > #title {
  opacity: 0;
}

body.toggled > #menu {
  opacity: 1;
}

body.toggled > #tiles > .tile:hover {
  opacity: 0.1 !important;
}

.centered {
  left: 50%;
  position: absolute;
  top: 50%;
  transform: translate(-50%, -50%);
}

#tiles {
  height: calc(100vh - 1px);
  width: calc(100vw - 1px);
  position: relative;
  z-index: 2;

  display: grid;
  grid-template-columns: repeat(var(--columns), 1fr);
  grid-template-rows: repeat(var(--rows), 1fr);
}

.tile {
  cursor: pointer;
  position: relative;
}

.tile:hover:before {
  background-color: rgb(30, 30, 30);
}

.tile:before {
  background-color: #24283b;
  content: "";
  inset: 0.5px;
  position: absolute;
}

#title {
  color: white;
  font-family: "Rubik", sans-serif;
  font-size: 4vw;
  margin: 0px;
  pointer-events: none;
  transition: opacity 800ms ease;
  width: 50vw;
  z-index: 3;
}



#menu {
  color: rgba(255, 255, 255, 0.15);
  font-size: 80vmin;
  opacity: 0;
  pointer-events: none;
  transition: opacity 800ms ease;
  z-index: 1;
}

#boom {
  position: absolute;
  width: 200px;
  height: 200px;

  background-size: cover;
  top: var(--top);
  left: var(--left);

  /*   opacity: var(--visible); */
  opacity: var(--visible);
  z-index: 109090;
  transform: translate(-35%, -40%);

}
.animate {
  animation: crash 6s linear;
}


@keyframes crash {
  0% {
    translate: -100vw;
    background-image: url("https://media.giphy.com/media/LKzGYwKzWtsfSPt2Wd/giphy.gif");
  }
  48% {
    background-image: url("https://media.giphy.com/media/LKzGYwKzWtsfSPt2Wd/giphy.gif");
  }
  49% {
    background-image: url("https://media.giphy.com/media/gJ1zlEIw4c30qpyooF/giphy.gif");
  }
  50% {
    translate: 0;
    background-image: url("https://media.giphy.com/media/gJ1zlEIw4c30qpyooF/giphy.gif");
  }

}

@keyframes break {
  50% {
    rotate: 0deg;
    color: white;
  }
  52% {
    rotate: 1deg;
    color: red;
  }
  54% {
    rotate: -1deg;
  }
  56% {
    rotate: 2deg;
  }
  58% {
    rotate: -2deg;
  }
  60% {
    rotate: 6deg;
    color: white;
  }
  100% {
    rotate: 6deg;
  }
}


@keyframes background-pan {
  from {
    background-position: 0% center;
  }

  to {
    background-position: -200% center;
  }
}

@keyframes scale {
  from, to {
    transform: scale(0);
  }

  50% {
    transform: scale(1);
  }
}

@keyframes rotate {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(180deg);
  }
}

body {
  background-color: rgb(10, 10, 10);
  display: grid;
  height: 100vh;
  margin: 0px;
  overflow: hidden;
  place-items: center;
}

h1 {
  color: white;
  font-family: "Rubik", sans-serif;
  font-size: clamp(2em, 2vw, 4em);
  font-weight: 400;
  margin: 0px;
  padding: 20px;
  text-align: center;
}

h1 > .magic {
  display: inline-block;
  position: relative;
}

h1 > .magic > .magic-star {
  --size: clamp(20px, 1.5vw, 30px);

  animation: scale 700ms ease forwards;
  display: block;
  height: var(--size);
  left: var(--star-left);
  position: absolute;
  top: var(--star-top);
  width: var(--size);
}

h1 > .magic > .magic-star > svg {
  animation: rotate 1000ms linear infinite;
  display: block;
  opacity: 0.7;
}

h1 > .magic > .magic-star > svg > path {
  fill: var(--violet);
}

h1 > .magic > .magic-text {
  animation: background-pan 3s linear infinite;
  background: linear-gradient(
    to right,
    var(--blue),
    var(--violet),
    var(--pink),
    var(--blue)
  );
  background-size: 200%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  white-space: nowrap;
}
</style>
