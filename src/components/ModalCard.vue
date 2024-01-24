<template>
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="logo fs-5">Add Note</h1>
        {{ inputTitle }}
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <form @submit.prevent="addNoteAndCloseModal" class="modal-body">
        <input class="form-control mb-2" type="text" :placeholder="data" v-model="inputTitle" />

        <textarea
          class="form-control"
          name=""
          id=""
          cols="30"
          rows="6"
          v-model="inputDescription"
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
  props: ['data'],
  data() {
    return {
      inputTitle: '',
      inputDescription: '',
      noteObject: {}
    }
  },
  methods: {
    addNoteAndCloseModal() {
      this.addNote() // Chama o método original para adicionar a nota
      this.closeModal() // Chama o método para fechar o modal
    },
    addNote() {
      ;(this.noteObject.id = 100),
        (this.noteObject.title = this.inputTitle),
        (this.noteObject.description = this.inputDescription),
        (this.noteObject.data = new Date('1984-11-17').toLocaleDateString())

      this.$emit('addNewNote', this.noteObject)
      this.noteObject = {}
      this.inputTitle = ''
      this.inputDescription = ''
    },
    closeModal() {
      // Adiciona lógica para fechar o modal aqui
      // Por exemplo, pode emitir um evento para o componente pai informando que o modal deve ser fechado
      this.$emit('closeModal')
    }
  }
}
</script>

<style lang="scss" scoped></style>
