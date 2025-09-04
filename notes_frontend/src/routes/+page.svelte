<script lang="ts">
  import Sidebar from "$lib/components/Sidebar.svelte";
  import Editor from "$lib/components/Editor.svelte";
  import { initNotes } from "$lib/stores/notes";

  // Initialize notes on page load
  initNotes();
</script>

<svelte:head>
  <title>NoteEase</title>
  <meta name="description" content="NoteEase - Minimalistic note taking app" />
</svelte:head>

<Sidebar />
<main class="main">
  <Editor />
</main>
