<script>
    import { page } from '$app/stores'; // import $page store from SvelteKit
    const links = [
        { text: "home", href: "/" },
        { text: "about", href: "/about" },
        { text: "projects", href: "/projects" },
    ];

    $: currentPath = $page.url.pathname;
</script>

<nav>
    <ul class="font-mono">
        {#each links as { href, text }}
            <li><a href={href}>{href === currentPath ? '* ':''}{text}</a></li>
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

    li:hover {
        text-decoration: underline;
    }

</style>
