<template>
  <div id="product">
    <div class="hero is-primary">
      <img :src="picture" />
      <div class="hero-body">
        <h1 class="subtitle">{{ title }}</h1>
      </div>
      <button class="button order" type="submit">
        <div class="shine"></div>Order
      </button>
      <button class="button is-danger comp" type="submit">
        <div class="shine"></div>Composition
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "product",
  props: {
    title: String,
    pic: String
  },
  computed: {
    picture() {
      return require("../assets/" + this.pic);
    }
  }
};
</script>

<style scoped lang="scss">
@mixin radius($r) {
  border-radius: $r;
  -webkit-border-radius: $r;
  -moz-border-radius: $r;
  -ms-border-radius: $r;
}
.hero {
  position: relative;
  height: 3em;
  line-height: 1em;
  padding: 0;
  @include radius(0.2em);
  .hero-body {
    background: rgb(168, 14, 214);
    height: 1em;
    line-height: 1em;
    padding: 0 0 3.4em 0;
    h1 {
      margin: 0;
      padding-top: 0.75em;
    }
  }
  button {
    position: absolute;
    z-index: -1;
    height: 2.3em;
    font-size: 1.1em;
    padding: 0 0.7em 0 0.7em;
    @include radius(0.2em);
  }
  .order {
    top: 810%;
    left: 3%;
    z-index: 2;
    padding: 0 1.8em 0 1.8em;
    background: rgb(255, 220, 23);
    color: rgb(0, 0, 0);
    border: none;
    box-shadow: 0 0em 0.15em 0.05em rgb(255, 246, 126);
    overflow: hidden;
    .shine {
      position: absolute;
      top: 0;
      left: 0;
      z-index: 2;
      opacity: 0.3;
      height: 100%;
      width: 100%;
      transform: skewX(-45deg);
      background: linear-gradient(to right, white, white 20px, transparent);
      transform-origin: left bottom;
      animation: shine 6s ease-in infinite;
    }
    &:hover {
      background: rgb(252, 255, 45);
    }
  }
  .comp {
    top: -109%;
    left: 0%;
    .shine {
      position: absolute;
      top: 0;
      left: 30%;
      z-index: 2;
      opacity: 0.3;
      height: 100%;
      width: 100%;
      transform: skewX(-45deg);
      background: linear-gradient(
        to right,
        rgba(251, 255, 2, 0.658),
        rgba(251, 255, 2, 0.658) 20px,
        transparent
      );
      transform-origin: left bottom;
    }
  }
}

@keyframes shine {
  0% {
    transform: skewX(-45deg) translateX(-100%);
  }
  20% {
    transform: skewX(-45deg) translateX(100%);
  }
  100% {
    transform: skewX(-45deg) translateX(100%);
  }
}

#product {
  margin-top: 9vh;
  height: 27em;
  background: rgba(173, 50, 255, 0.185);
  @include radius(0.1em);
  z-index: 1;
  img {
    margin-top: -0.3em;
    z-index: 1;
    min-height: 24.2em;
  }
  transition: transform 0.4s;
  &:hover {
    cursor: pointer;
  }
}

@media (max-width: 4000px) {
  #product {
    width: 32em;
    margin-left: calc((100% - 96em) / 6);
    margin-right: calc((100% - 96em) / 6);
  }
}

@media (max-width: 1400px) {
  #product {
    width: 32em;
    margin-left: calc((100% - 64em) / 4);
    margin-right: calc((100% - 64em) / 4);
  }
}

@media (max-width: 980px) {
  #product {
    margin-top: 15vh;
    width: 36em;
    height: 30em;
    img {
      min-height: 27.4em;
    }
    margin-left: calc((100% - 36em) / 2);
    margin-right: calc((100% - 36em) / 2);
  }
}

@media (max-width: 660px) {
  #product {
    width: 90%;
    min-height: 23em;
    margin-left: 5%;
    margin-right: 0;
  }
}
</style>
