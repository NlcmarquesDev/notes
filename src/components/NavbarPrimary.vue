<script>
import { RouterLink, RouterView } from 'vue-router'
export default {}
</script>

<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container-fluid">
      <RouterLink class="navbar-brand logo" to="/">NOTES</RouterLink>

      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav ms-auto">
          <RouterLink class="btn btn-primary login" to="/login">Login</RouterLink>
        </div>
      </div>
    </div>
  </nav>
  <RouterView />
</template>

<style lang="scss" scoped>
.login {
  color: blue;
}
</style>
