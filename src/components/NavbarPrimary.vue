<script>
// import { RouterLink, RouterView } from 'vue-router'
export default {}
</script>

<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container-fluid">
      <a class="navbar-brand logo" href="/">NOTES</a>

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
          <a class="btn btn-primary login" href="/login">Login</a>
        </div>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
.login {
  color: blue;
}
</style>
