<template>
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="logo fs-5">Add Note</h1>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <form @submit.prevent="addNote" class="modal-body">
        <input class="form-control mb-2" type="text" v-model="inputTitle" placeholder="Title..." />

        <textarea
          class="form-control"
          name=""
          id=""
          cols="30"
          rows="6"
          v-model="inputDescription"
          placeholder="Description ..."
        ></textarea>
        <div class="modal-footer">
          <button type="submit" class="btn btn-secondary" data-bs-dismiss="modal">Save</button>
          <button type="button" class="btn btn-danger" data-bs-dismiss="modal">Cancel</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  props: ['userTitle', 'userDescription'],
  data() {
    return {
      inputTitle: this.userTitle,
      inputDescription: this.userDescription,
      noteObject: {}
    }
  },
  methods: {
    addNote() {
      console.log(this.userTitle)
      ;(this.noteObject.id = 100),
        (this.noteObject.title = this.inputTitle),
        (this.noteObject.description = this.inputDescription),
        (this.noteObject.data = new Date('1984-11-17').toLocaleDateString())

      this.$emit('addNewNote', this.noteObject)
      this.noteObject = {}
      this.inputTitle = ''
      this.inputDescription = ''
    }
  }
  // watch: {
  //   userData: {
  //     handler(newVal) {
  //       console.log(newVal)
  //       // Atualiza os campos do formulário quando a propriedade 'userData' muda
  //       // this.inputTitle = newVal.title
  //       // this.inputDescription = newVal.description
  //     }
  //     // immediate: true // Chama o handler imediatamente após a criação do componente
  //   }
  // }
}
</script>

<style lang="scss" scoped></style>
