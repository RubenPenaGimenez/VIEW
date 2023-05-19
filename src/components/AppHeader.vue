<template>
  <header class="main-header">
    <nav class="navbar navbar-light navbar-header">
      <div class="container">
        <div class="logo">
          <router-link to="/">
            <img src="../../src/assets/logos/logo.svg" class="img-fluid logo-img logo-img--full" alt="logo">
            <img src="../../src/assets/logos/logo.png" class="img-fluid logo-img logo-img--mobile" alt="logo">
          </router-link>
        </div>
        <form class="search">
          <input class="form-control" type="search" placeholder="Search for a product or inspiration">
          <div class="search__icon">
            <i class="fas fa-search"></i>
          </div>
        </form>
        <div class="user-options">
          <div class="user-options__item">
            <router-link to="/cart" aria-label="Cart" class="nav-link"><i class="fas fa-cart-shopping fa-xl"></i></router-link>
          </div>
          <div class="user-options__item">
            <a href="/login" aria-label="User" class="nav-link"><i class="fas fa-user fa-xl"></i></a>
          </div>
        </div>
      </div>
    </nav>

    <nav class="navbar navbar-expand-lg navbar-categories">
      <div class="container">
        <router-link to="/" class="navbar-brand">Top categories</router-link>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link to="/categories/smartphones" class="nav-link">Smartphones</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/categories/laptops" class="nav-link">Laptops</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/categories/fragances" class="nav-link">Fragances</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/categories/skincare" class="nav-link">Skincare</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/categories/groceries" class="nav-link">Groceries</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/categories/home-decoration" class="nav-link">Home decoration</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>


<script>
import SearchBar from "./SearchBar.vue";

export default {
  name: "AppHeader",
  components: {
    SearchBar
  },
};
</script>

<style>
/* Estilos para la cabecera */
</style>
