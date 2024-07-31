<template>
  <div>
    <Navbar />
    <div class="container">
      <div class="row mt-4">
        <div class="col">
          <h2>Daftar <strong>Makanan</strong></h2>

          <div class="row mt-3">
            <div class="col">
              <b-input-group size="md">
                <b-form-input placeholder="Cari makanan favorit anda..." aria-label="Cari" v-model="search" @keyup="searchFood"></b-form-input>
                <div class="input-group-prepend">
                  <span class="input-group-text">
                    <b-icon-search></b-icon-search>
                  </span>
                </div>
              </b-input-group>
            </div>
          </div>

          <div class="row mb-4">
            <div
              class="col-md-4 mt-4"
              v-for="product of products"
              :key="product.id"
            >
              <CardProduct :product="product" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import CardProduct from "@/components/CardProduct.vue";
import axios from "axios";

export default {
  name: "FoodsView",
  components: {
    Navbar,
    CardProduct,
  },
  data() {
    return {
      products: [],
      search: "",
    };
  },
  methods: {
    setProducts(data) {
      this.products = data;
    },
    searchFood() {
      axios
      .get("http://localhost:3000/products?q="+this.search)
      .then((response) => this.setProducts(response.data))
      .catch((error) => console.log(error));
    }
  },
  mounted() {
    axios
      .get("http://localhost:3000/products")
      .then((response) => this.setProducts(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
</style>