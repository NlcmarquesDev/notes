<template>
  
<!-- Button trigger modal -->
<button type="button" class="cardItem d-flex flex-column justify-content-between" data-bs-toggle="modal" data-bs-target="#exampleModal">
  <div >
    <h1 class="title-card logo ">Title from the Note</h1>
    <p class="title-card__text">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum dolorem dicta nam nihil aperiam asperiores. Placeat accusantium velit saepe earum.</p>
  </div>
  <p class="title-card__date "> 06/09/2023 6:00 p.m</p>
</button>

<!-- Modal -->
<ModalCard/>
</template>

<script setup>
import ModalCard from './ModalCard.vue';

</script>

<style lang="scss" scoped>
.title-card{
  font-size: 1.75rem;
  padding:0 5px;
  color:$primary;
  padding-top: 20px;
  &__text{
    padding:0 5px;
  }
  &__date{
    margin-left: auto;
    font-size:0.75rem;
    color: grey;
  }

}
.cardItem{
  width: 350px;
  height: 250px;
  border: 1px solid $primary ;
  border-radius: 10px;
  box-shadow: 5px 5px 5px rgb(197, 196, 196) ;
  background-color: transparent;
  text-align: left;
}

</style>