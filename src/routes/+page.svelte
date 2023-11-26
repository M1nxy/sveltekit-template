<script lang="ts">
  let greeting: string = "Hello World!";
</script>

<svelte:head>
  <title>
    {greeting}
  </title>
  <meta name="description" content="Basic demo site for github pages and sveltekit.">
</svelte:head>
<main>
  <div class="greeting">
    <h1>{greeting}</h1>
  </div>
</main>

<style>
  main {
    font-family:
      system-ui,
      -apple-system,
      BlinkMacSystemFont,
      "Segoe UI",
      Roboto,
      Oxygen,
      Ubuntu,
      Cantarell,
      "Open Sans",
      "Helvetica Neue",
      sans-serif;
    height: 100%;
  }
</style>
