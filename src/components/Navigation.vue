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
          <div
            role="button"
            aria-label="navbarMenu"
            aria-expanded="false"
            class="navbar-burger burger"
            data-target="navbarMenu"
            @click="activateMenu"
          >
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </div>
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
            <a class="navbar-item has-dropdown is-hoverable categories" @click="toggleCategories">
              <a class="navbar-link">Categories</a>
              <div class="navbar-dropdown is-primary">
                <a class="navbar-item">Fruit Cakes</a>
                <a class="navbar-item">Chocolate Cakes</a>
                <a class="navbar-item">Cookies</a>
              </div>
            </a>
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
  props: {},
  methods: {
    activateMenu() {
      document.querySelector(".burger").classList.toggle("is-active");
      document.querySelector("#navbarMenu").classList.toggle("is-active");
    },
    toggleCategories() {
      document.querySelector(".categories").classList.toggle("is-active");
    }
  }
};
</script>

<style scoped lang="scss">
.navbar {
  box-shadow: 0 0.15em 0.6em 0 rgba(73, 73, 73, 0.301);
}

.burger {
  z-index: 5;
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
  .navbar-dropdown {
    border-radius: 0.4em;
    font-size: 1.05em;
  }
  &.has-dropdown {
    .navbar-dropdown {
      display: none;
    }
    &.is-active {
      .navbar-dropdown {
        display: block;
      }
    }
  }
}
.hero {
  padding: 1.5em 0 1.5em;
  h1 {
    margin-bottom: 1.1em;
  }
}
</style>
