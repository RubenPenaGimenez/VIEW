<template>
  <div>
    <AppHeader />
    <HomeView />
    <router-view />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import HomeView from "./views/HomeView.vue"

export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter,
    HomeView
  }
};
</script>
