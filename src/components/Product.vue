<template>
  <div id="product">
    <div class="hero is-primary">
      <div class="hero-body">
        <h1 class="subtitle">{{ title }}</h1>
      </div>
      <img :src="picture" />
      <button class="button is-warning order" type="submit">Order</button>
      <button class="button is-danger comp" type="submit">Composition</button>
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
    padding-top: 0em;
    height: 1em;
    line-height: 1em;
    h1 {
      margin: 0;
      padding-top: 0.6em;
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
    top: 124%;
    left: 3%;
  }
  .comp {
    top: -100%;
    left: 0%;
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
    z-index: -1;
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
