<script lang="ts">
    import { page } from '$app/stores';
</script>
<svelte:head>
    <title>{$page.status} - {$page.error ? $page.error.message : 'Not Found!'}</title>
</svelte:head>
<main>
    <div class="error">
        <span class="status">{$page.status}</span>
        <div class="message">
            <h1>{$page.error ? $page.error.message : 'Not Found!'}</h1>
        </div>
    </div>
    <a href="/">Return Home!</a>
</main>

<style>
    main {
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .error {
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0 1rem;
    }
    .status {
        font-weight: 200;
        font-size: 3rem;
        line-height: 1;
        position: relative;
        top: -0.05rem;
    }
    .message {
        border-left: 1px solid #ccc;
        padding: 0 0 0 1rem;
        margin: 0 0 0 1rem;
        min-height: 2.5rem;
        display: flex;
        align-items: center;
    }
    .message > h1 {
        font-weight: 400;
        font-size: 1em;
        margin: 0;
    }
    a {
        transition: text-decoration 100ms ease-in-out;
        text-decoration: underline;
        text-decoration-color: transparent;
    }
    a:hover {
        text-decoration-color: currentColor;
    }
</style>
