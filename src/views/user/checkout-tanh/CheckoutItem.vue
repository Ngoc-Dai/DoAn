<template>
  <li class="product-checkout">
    <div class="image">
      <img
        :src="require('../../../assets'.concat(image))"
        style="max-width: 64px; border: 1px solid #ccc; border-radius: 5px"
        alt=""
      />
      <div class="quantity">{{ quantity }}</div>
      <div class="product-info">
        <div class="title">{{ title }}</div>
        <div class="info-detail">
          <span class="size">{{ size }}</span>
          <span> / </span>
          <span class="color"> {{ color }} </span>
          <span> / </span>
          <span class="material"> {{ material }} </span>
        </div>
      </div>

      <div class="price">{{ price }} ₫</div>
    </div>
  </li>
</template>

<script>
export default {
  props: [
    "id",
    "title",
    "size",
    "color",
    "material",
    "quantity",
    "price",
    "image",
  ],

  name: "checkout-item",

  components: {},
};
</script>

<style scoped>
.product-checkout {
  background-color: #fafafa;
  padding: 0px;
  margin: 0px;
  list-style: none;
  padding-top: 16px;
}
.product-checkout .image {
  position: relative;
  display: flex;
}
.product-checkout .image .quantity {
  width: 21px;
  height: 21px;
  border: 1px solid #ccc;
  background-color: rgba(114, 114, 114, 0.9);
  border-radius: 50%;
  text-align: center;
  color: white;
  position: absolute;
  top: -12px;
  left: 54px;
}
.product-checkout .image .product-info {
  margin-left: 20px;
}
.product-info .title {
  margin-top: 8px;
}

.product-info .info-detail {
  margin-top: 4px;
  font-size: 12px;
}
.image .price {
  position: absolute;
  right: 0px;
  top: 24px;
}
</style>
