<template>
  <div class="product-item">
    <img :src="`/assets/${product.image}`" class="product-image" />
    <p class="product-price">{{ product.price }}</p>
    <i v-if="status ==1" class="bi bi-check-circle-fill"></i>
    <i v-else class="bi bi-check-circle"></i>
    <h3>{{ product.name }}</h3>

    <p class="product-description">{{ product.description }}</p>
    <div class="product-rating">
      <span
        v-for="rate in product.rating"
        :key="`full-${rate}-${product.id}`"
        class="filled-star"
      >&#9733;</span>
      <span
        v-for="star in 5 - Math.ceil(product.rating)"
        :key="`empty-${star}-${product.id}`"
        class="empty-star"
      >&#9734;</span>
    </div>
  </div>
</template>




<script>
export default {
  name: "ProductItem",
  props: {
    product: Object
  }
};
</script>

<style>
.product-item {
  padding: 1rem;
  margin: 1rem;
  width: 300px;
  text-align: center;
}

.product-image {
  max-width: 100%;
  height: auto;
  margin-bottom: 1rem;
}

.produkt_beschreibung {
  min-height: 60px;
}

.product-rating {
  color: #ffd700;
  font-size: 1rem;
  margin-bottom: 0.5rem;
}

.filled-star {
  color: #5f5f5e;
}

.empty-star {
  color: #ccc;
}

.product-price {
  color: red;
  font-weight: bold;
  font-size: 1.2rem;
  margin-top: 0.5rem;
}
</style>