<template>
  <div v-for="note in data" :key="data.id">
    <!-- Button trigger modal -->
    <button
      type="button"
      class="cardItem d-flex flex-column justify-content-between"
      data-bs-toggle="modal"
      :data-bs-target="'#cardModal_' + note.id"
    >
      <div>
        <h1 class="title-card logo">{{ note.title }}</h1>
        <p class="title-card__text">
          {{ note.description }}
        </p>
      </div>
      <p class="title-card__date">{{ note.date }}</p>
    </button>

    <!-- Modal -->
    <div
      class="modal fade"
      :id="'cardModal_' + note.id"
      tabindex="11"
      aria-labelledby="exampleModalLabel"
    >
      <ModalCard :userTitle="note.title" :userDescription="note.description" />
    </div>
  </div>
</template>

<script>
import ModalCard from './ModalCard.vue'
export default {
  components: {
    ModalCard
  },
  props: ['data'],
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.title-card {
  font-size: 1.75rem;
  padding: 0 5px;
  color: $primary;
  padding-top: 20px;
  &__text {
    padding: 0 5px;
  }
  &__date {
    margin-left: auto;
    font-size: 0.75rem;
    color: grey;
  }
}
.cardItem {
  width: 350px;
  height: 250px;
  border: 1px solid $primary;
  border-radius: 10px;
  box-shadow: 5px 5px 5px rgb(197, 196, 196);
  background-color: transparent;
  text-align: left;
}
</style>
