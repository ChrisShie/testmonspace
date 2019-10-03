<template>
  <b-navbar toggleable="lg" fixed>
    <b-navbar-brand href="#">E-commerce</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="#">Kategori</b-nav-item>
      </b-navbar-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-form>
          <b-input-group style="width: 800px;">
            <b-form-input placeholder="Cari produk atau toko"></b-form-input>
            <b-input-group-append>
              <b-button><i class="fas fa-search"></i></b-button>
            </b-input-group-append>
          </b-input-group>
        </b-nav-form>
      </b-navbar-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#">
          <i class="fas fa-shopping-cart"></i> |
        </b-nav-item>
        <b-nav-item href="#">Masuk</b-nav-item>
        <b-nav-item href="#">Daftar</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  data () {
    return {
      search: false,
      searchText: undefined
    }
  }
}
</script>

<style>
</style>
