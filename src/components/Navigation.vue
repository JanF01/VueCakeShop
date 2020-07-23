<template>
  <div>
    <div class="navbar">
      <div class="container">
        <div class="navbar-brand">
          <a class="navbar-item">
            <img
              src="../assets/bakery.png"
              style="transform:rotateY(180deg);filter:grey-scale(100%)"
            />
            <h1 class="subtitle">Bakery</h1>
          </a>
          <a class="navbar-item"></a>
          <span class="navbar-burger burger" data-target="navbarMenu">
            <span></span>
            <span></span>
            <span></span>
          </span>
        </div>
        <div id="navbarMenu" class="navbar-menu">
          <div class="navbar-end">
            <a class="navbar-item">
              <img
                src="../assets/shopping-cart.png"
                style="transform:rotateY(180deg);filter:grey-scale(100%)"
              />
            </a>
            <a class="navbar-item is-active">Home</a>
            <a class="navbar-item">Categories</a>
            <a class="navbar-item">Contact us</a>
          </div>
        </div>
      </div>
    </div>
    <div class="hero is-primary">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title">CupCakes</h1>
          <h2 class="subtitle">Have you ever fainted, couse of taste delightenment?</h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "navigation",
  props: {}
};
</script>

<style scoped lang="scss">
.navbar {
  box-shadow: 0 0.15em 0.6em 0 rgba(73, 73, 73, 0.301);
}
.navbar-item {
  img {
    width: 2em;
  }
  .subtitle {
    color: white;
    font-size: 1.5em;
    margin: 0.14em 0 0 0.2em;
  }
}
.hero {
  padding: 1.5em 0 1.5em;
  h1 {
    margin-bottom: 1.1em;
  }
}
</style>
