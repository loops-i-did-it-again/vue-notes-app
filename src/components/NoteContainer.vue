<template>
  <div class="note-container">
    <NoteSelectors v-bind:notes="notes" />
    <NoteEditor />
  </div>
</template>

<script>
import NoteSelectors from "./NoteSelectors";
import NoteEditor from "./NoteEditor";
export default {
  components: {
    NoteSelectors,
    NoteEditor,
  },
  props: ["notes"],
};
</script>
