<template>
  <div class="hero">
    <!-- Desktop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Delicious Food Menu,</strong> <br />
                in Your Gadget
              </h2>
              <p>Ayo segera pilih dan pesan makanan favorit Anda</p>
              <router-link class="btn btn-lg btn-success" to="/foods">
                <b-icon-arrow-right></b-icon-arrow-right> Pesan
              </router-link>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/hero.png" width="100%" alt="hero" />
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <div class="d-md-none d-sm-block">
      <div class="row mt-4">
        <div class="col">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <div class="col-md-6 mb-3">
                <img src="../assets/hero.png" width="100%" alt="hero" />
              </div>
              <h2>
                <strong>Delicious Food Menu,</strong> <br />
                in Your Gadget
              </h2>
              <p>Ayo segera pilih dan pesan makanan favorit Anda</p>
              <button class="btn btn-lg btn-success">
                <b-icon-arrow-right></b-icon-arrow-right> Pesan
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroCom",
};
</script>

<style>
</style>