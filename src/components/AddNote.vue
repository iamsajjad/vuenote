<template>
  <div class="is-centered columns is-vcentered">
    <div class="add-note is-flex  box">
      <form @submit.prevent="submitNote">
        <input v-model="text" class="input" type="text" placeholder="Note here ...">
        <input v-model="date" class="date" type="date"> {{text}}
        <button class="button is-warning">Add Note</button>
      </form>
    </div>
  </div>
</template>

<script lang="ts">



import { Options, Vue } from 'vue-class-component';

@Options({
  name: 'AddNote',
  data() {
    return {
      text: '',
      date: '',
    }
  },
  methods: {
    submitNote(e : Event) {
      console.log(this.text);

      if (!this.text) {
        alert("Please Enter Note and Date");
        return
      }
      const NewNote = {
        text: this.text,
        date: this.date,
      }
    }
  },
})
export default class AddNote extends Vue {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.add-note {
  margin: 50px 0;
  width: 650px;
}
button {
  margin: 0 20px;
}
</style>
