<template>
  <nav class="navbar navbar-expand-lg border-bottom">
  <div class="container-fluid">
    
    <a class="brand rounded-circle" href="/dashboard"><span class="letter">N</span></a>
    <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-secondary" type="submit">Search</button>
      </form>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse " id="navbarSupportedContent">
      <a class="ms-auto btn btn-primary" href="/logout">Logout</a>
    </div>
  </div>
</nav>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.brand{
  background-color: $primary;
  margin-right: 20px;
  padding:20px;
  position: relative;
  z-index: 0;
  border: 2px solid black;
}
span{
  position: absolute;
  z-index: 99;
  bottom: -5px;
  left : 9px;
  font-size: 2rem;
  color: white;
}
.navbar{
  position: fixed;
}
</style>