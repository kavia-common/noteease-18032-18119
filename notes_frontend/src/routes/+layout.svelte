<script lang="ts">
  import "../app.css";
  import "$lib/styles/theme.css";
  let { children } = $props();
</script>

<div class="app-shell">
  {@render children()}
</div>
