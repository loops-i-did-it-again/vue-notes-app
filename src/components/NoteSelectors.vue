<template>
  <div class="note-selectors">
    <NoteSelector
      v-for="note in notes"
      v-bind:note="note"
      v-bind:selectedNoteId="selectedNoteId"
      v-bind:key="note.id"
      v-on:selectNote="selectNote"
    />
  </div>
</template>

<script>
import NoteSelector from "./NoteSelector";
export default {
  components: {
    NoteSelector,
  },
  props: ["notes"],
  data: function() {
    return {
      selectedNoteId: 1,
    };
  },
  methods: {
    selectNote: function(note) {
      this.selectedNoteId = note.id;
    },
  },
};
</script>
