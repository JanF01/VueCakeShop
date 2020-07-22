<template>
  <nav>
   <h3>
    Welcome to Cake Shop
   </h3>
  </nav>
</template>

<script>
export default {
  name: "navigation",
  props: {
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
nav{
  width:100%;
  h3{
    margin: 0 auto;
    width:20%;
    font-size:1.3em;
    color:darkgrey;
    font-family:Sans-serif;
  }
}
</style>
