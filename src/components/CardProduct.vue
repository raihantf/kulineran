<template>
  <div class="card shadow card-product">
    <b-card :img-src="'../assets/images/' + product.gambar" img-top class="img-top">
      <h5>{{ product.nama }}</h5>
      <b-card-text>
        Harga : Rp. {{ product.harga }}
      </b-card-text>
      <router-link :to="'/foods/' +  product.id " class="btn btn-success"><b-icon-cart></b-icon-cart> Pesan</router-link>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "CardProduct",
  props: ["product"],
};
</script>

<style>
</style>