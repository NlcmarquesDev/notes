<script setup>
import { RouterLink } from 'vue-router'
import NavbarPrimary from './../components/NavbarPrimary.vue'
</script>

<template>
 
  <NavbarPrimary/>
  
  <main class="home">
    <div>
      <h1 class="logo fs-1">
        Write your thoughts <br />
        down as they come to <br />
        you.
      </h1>
      <p>Notes is free note taking application...</p>
      <div>
        <RouterLink class="btn btn-primary login me-3" to="/login">Login</RouterLink>
        <RouterLink class="btn btn-secondary login text-success" to="/register">Register</RouterLink>
      </div>
    </div>
    <img src="@/images/giphy.gif" alt="" />
  </main>
  
</template>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: column-reverse;
  justify-content: center;
  align-items: center;
  height: calc(100vh - 108px);
}
@media (min-width: 992px) {
  .home {
    display: flex;
    flex-direction: initial;
    justify-content: space-between;
    align-items: center;
  }
}
</style>