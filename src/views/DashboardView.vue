<script>
import NavbarDashboard from '../components/NavbarDashboard.vue'
import CardItem from '../components/cardItem.vue'
import ModalCard from '../components/ModalCard.vue'
export default {
  components: {
    ModalCard,
    CardItem
  },
  data() {
    return {
      username: 'Nuno',
      notes: [
        {
          id: 1,
          title: 'Working on Vue',
          description: 'This is the text for a description for a notes App.',
          date: new Date('1984-11-17').toLocaleDateString()
        },
        {
          id: 2,
          title: 'Go to Gym',
          description:
            'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum dolorem dicta nam nihilaperiam asperiores. Placeat accusantium velit saepe earum.',
          date: new Date('1984-11-17').toLocaleDateString()
        },
        {
          id: 3,
          title: 'Repplace my mouse',
          description: 'This is the text for a description for a notes App.',
          date: new Date().toLocaleDateString()
        },
        {
          id: 4,
          title: 'Try add new features on the portfolio',
          description:
            'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum dolorem dicta nam nihilaperiam asperiores. Placeat accusantium velit saepe earum.',
          date: new Date('1984-11-17').toLocaleDateString()
        },
        {
          id: 5,
          title: "Don't give up",
          description: 'This is the text for a description for a notes App.',
          date: new Date('1984-11-17').toLocaleDateString()
        }
      ]
    }
  },
  methods: {
    addNewData(data) {
      this.notes.push(data)
    }
  }
}
</script>

<template>
  <NavbarDashboard />
  <main class="notes">
    <div class="d-flex justify-content-between">
      <div>
        <h1 class="logo fs-1">
          Hey, <span>{{ username }}</span>
        </h1>
      </div>
      <button
        class="btn btn-primary"
        type="button"
        data-bs-toggle="modal"
        data-bs-target="#addModal"
      >
        + Add New
      </button>
      <div class="modal fade" id="addModal" tabindex="11" aria-labelledby="exampleModalLabel">
        <ModalCard @addNewNote="addNewData" />
      </div>
    </div>
    <section class="pt-4 d-flex justify-content-evenly flex-wrap gap-4">
      <CardItem :data="notes" />
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
.logo {
  color: $primary;
  padding-top: 15px;
}
span {
  color: black;
}
button {
  margin: 15px 0;
}
</style>
