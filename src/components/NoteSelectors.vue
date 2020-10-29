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
  data: function() {
    return {
      notes: [
        { id: 1, body: "This is the first note", timestamp: Date.now() },
        { id: 2, body: "This is the second note", timestamp: Date.now() },
        { id: 3, body: "This is the third note", timestamp: Date.now() },
        { id: 4, body: "This is the fourth note", timestamp: Date.now() },
        { id: 5, body: "This is the fifth note", timestamp: Date.now() },
      ],
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
