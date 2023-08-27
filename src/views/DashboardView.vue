<script setup>
import NavbarDashboard from '../components/NavbarDashboard.vue';
import CardItem from '../components/CardItem.vue';
import ModalCard from '../components/ModalCard.vue';

</script>

<template>
  <NavbarDashboard  />
  <main class="notes">
    <div class="d-flex justify-content-between">
      <div>
        <h1 class="logo fs-1 ">Hey, <span>Test</span></h1>
      </div>
      <button class="btn btn-primary" type="button" data-bs-toggle="modal" data-bs-target="#exampleModal">+ Add New
        <ModalCard/>
      </button>
    </div>
    <section class="pt-4 d-flex justify-content-evenly flex-wrap gap-4">
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
      <CardItem/>
    </section>
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
.logo{
  color: $primary;
  padding-top: 15px;
}
span{
  color: black;
}
button{
  margin: 15px 0 ;
}
</style>
