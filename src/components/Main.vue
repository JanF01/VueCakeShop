<template>
  <div id="main">
    <product title="Ciasto Murzynek" picture="/img/birthday_cake.66655a2f.jpg"></product>
    <product title="Tort Urodzinowy" picture="/img/birthday_cake.66655a2f.jpg"></product>
    <product title="Ciasteczka Czekoladowe" picture="/img/birthday_cake.66655a2f.jpg"></product>
  </div>
</template>


<script>
import Product from "./Product";
export default {
  name: "main",
  props: {},
  components: {
    Product
  }
};
</script>

<style scoped lang="scss">
#main {
  display: flex;
  flex-wrap: wrap;
  min-height: 90vh;
  background: rgba(255, 255, 255, 0.973);
}
</style>