<template>
  <div id="app">
    <Title />
    <ProductList :products="products" />
    <Footer />
  </div>
</template>

<script>
import Title from "./components/Title.vue";
import ProductList from "./components/ProductList.vue";

export default {
  name: "App",
  components: {
    Title,
    ProductList
  },
  data() {
    return {
      products: [
        {
          id: 1,
          name: "Playstation 5",
          description: "Playstation 5 Slim Disc Edition",
          price: "508.-",
          rating: 4,
          status: 1,
          image: "ps5.jpeg"
        },
        {
          id: 2,
          name: "Meta Quest 3 128 GB",
          description: "Enhance the world with Meta Quest 3",
          price: "502.-",
          rating: 2,
          status: 2,
          image: "quest.jpeg"
        },
        {
          id: 3,
          name: "Microsoft Xbox Series X",
          description: "A brand new way of gaming",
          price: "389.-",
          rating: 3,
          status: 1,
          image: "x.jpeg"
        }
      ]
    };
  }
};
</script>

<style>
body {
  background-color: #fff;
  color: #000;
}
</style>