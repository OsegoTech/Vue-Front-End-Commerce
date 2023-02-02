<template>
  <div class="grid-wrap">
    <ProductsGridItem
      v-for="product in products"
      :key="product.id"
      :product="product"
    />
  </div>
</template>

<script>
import ProductsGridItem from "@/components/ProductGridItem.vue";

export default {
  name: "ProductsGrid",
  props: ['products'],
  components: {ProductsGridItem}
}
</script>

<style scoped>
.grid-wrap {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 16px;
}

.product-item {
  align-items: center;
  border-radius: 8px;
  box-shadow: 0 2px 5px #888;
  display: flex;
  flex-direction: column;
  margin-bottom: 2%;
  padding: 20px;
  position: relative;
  width: 32%;
}

</style>