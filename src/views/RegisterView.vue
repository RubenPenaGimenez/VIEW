<template>
  <main class="page-register container main-body">
    <section class="box-auth">
      <div class="box-auth__form">
        <h1 class="main-title">Register</h1>
        <p class="auth-intro">Not a member? sign up today</p>

        <form @submit.prevent="register">
          <div class="form-group">
            <label class="form-label" for="username">E-mail</label>
            <input
              placeholder="E-mail"
              type="email"
              id="email"
              class="form-control"
              v-model="email"
            />
          </div>
          <div class="form-group">
            <label class="form-label" for="password">Password</label>
            <input
              placeholder="Password"
              type="password"
              id="password"
              class="form-control"
              v-model="password"
            />
          </div>
          <button type="submit" class="btn btn-primary btn-lg mt-3">
            Register
          </button>

        </form>

        <p class="auth-bottom">
          Already have an account?
          <router-link to="/login" class="alink">Sign in</router-link>
        </p>
      </div>
    </section>
  </main>
</template>

<script>
import { getAuth, createUserWithEmailAndPassword } from "firebase/auth";

export default {
  name: "RegisterView",
  data: function () {
    return {

    };
  },
  methods: {
    register: function (e) {
      const auth = getAuth();
      createUserWithEmailAndPassword()
      e.preventDefault();
    },
  },
};
</script>
<style lang="scss" scoped>
.container {
  max-width: 500px;
}
</style>