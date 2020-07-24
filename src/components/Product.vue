<template>
  <div id="product">
    <div class="hero is-primary">
      <div class="hero-body">
        <h1 class="subtitle">{{ title }}</h1>
      </div>
      <img :src="picture" />
    </div>
  </div>
</template>

<script>
export default {
  name: "product",
  props: {
    title: String,
    picture: String
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
  height: 3em;
  line-height: 1em;
  padding: 0;
  @include radius(0.2em);
  .hero-body {
    padding-top: 0.8em;
    height: 1em;
    line-height: 1em;
    h1 {
      margin: 0;
    }
  }
}
#product {
  margin-top: 7vh;
  height: 28em;

  background: rgba(173, 50, 255, 0.185);
  @include radius(0.1em);
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
    width: 36em;
    margin-left: calc((100% - 36em) / 2);
    margin-right: calc((100% - 36em) / 2);
  }
}

@media (max-width: 660px) {
  #product {
    width: 100%;
    margin-left: 0;
    margin-right: 0;
  }
}
</style>
