<template>
  <the-header></the-header>
  <router-view></router-view>
</template>

<script>
import TheHeader from './components/nav/TheHeader.vue';

export default {
  components: {
    TheHeader,
  },
  data() {
    return {
      //authentication state
      isLoggedIn: false,
    };
  },
  provide() {
    return {
      isLoggedIn: this.isLoggedIn,
      // products: this.products,
      cart: this.cart,
      addProductToCart: this.addProductToCart,
      removeProductFromCart: this.removeProductFromCart,
      login: this.login,
      logout: this.logout,
    };
  },
  methods: {
    login() {
      this.isLoggedIn = true;
      console.log('Log In');
      console.log(this.isLoggedIn);
    },
    logout() {
      this.isLoggedIn = false;
      console.log('Log Out');
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>
