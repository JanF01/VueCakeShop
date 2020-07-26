<template>
  <div id="products">
    <product title="Ciasto Murzynek" pic="cake.jpg"></product>
    <product title="Tort Urodzinowy" pic="birthday_cake.jpg"></product>
    <product title="Ciasteczka Czekoladowe" pic="cookies.jpg"></product>
    <product title="Tort Urodzinowy" pic="birthday_cake.jpg"></product>
    <product title="Ciasteczka Czekoladowe" pic="cookies.jpg"></product>
    <product title="Ciasto Murzynek" pic="cake.jpg"></product>
    <product title="Ciasteczka Czekoladowe" pic="cookies.jpg"></product>
  </div>
</template>


<script>
import Product from "./Product";
export default {
  name: "products",
  props: {},
  components: {
    Product
  }
};
</script>

<style scoped lang="scss">
#products {
  display: flex;
  flex-wrap: wrap;
  min-height: 110vh;
  background: rgba(255, 255, 255, 0.973);
  margin-bottom: 10vh;
}
</style>