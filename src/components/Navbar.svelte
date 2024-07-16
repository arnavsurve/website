<script>
    import { page } from '$app/stores'; // import $page store from SvelteKit
    const links = [
        { text: "home", href: "/" },
        { text: "projects", href: "/projects" },
        { text: "resume", href: "/resume" },
        { text: "misc", href: "/misc" },
    ];

    $: currentPath = $page.url.pathname;
</script>

<nav>
    <ul class="font-mono">
        {#each links as { href, text }}
            <li><a href={href} class="hover:underline">{href === currentPath ? '* ':''}{text}</a></li>
        {/each}
    </ul>
</nav>

<style>
    nav {
        display: flex;
        justify-content: space-between;
        padding: 1rem;
    }

    /* ul {
        margin-left: auto;
    } */
</style>
