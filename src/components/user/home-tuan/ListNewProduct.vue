<template>
  <div class="container-list">
    <div class="container-title">
      Sản phẩm mới
    </div>

    <v-app>
      <v-sheet class="mx-auto" max-width="90%">
        <v-slide-group class="pa-4" show-arrows>
          <v-slide-item v-for="(item, index) in listNewProduct" :key="index">
            <!-- product -->

            <SingleProduct :product="item" />
          </v-slide-item>
        </v-slide-group>
      </v-sheet>
    </v-app>
  </div>
</template>

<script>
import SingleProduct from "./SingleProduct.vue";

export default {
  components: { SingleProduct },

  props: {
    listNewProduct: Array,
  },

  data: () => ({}),
};
</script>

<style>
.container-list {
  padding-top: 40px;
  width: 100%;
  min-height: 120px;
}
.container-title {
  width: 100%;
  height: 60px;
  line-height: 60px;
  font-weight: 700;
  font-size: 36px;
  text-transform: uppercase;
  padding: 0px 10px;
  border-left: 8px solid var(--background-dark);
}
</style>
