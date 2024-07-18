<script>
    import { page } from '$app/stores'; // import $page store from SvelteKit
    const links = [
        { text: "home", href: "/" },
        { text: "projects", href: "/projects" },
        { text: "resume", href: "/resume" },
        { text: "misc", href: "/misc" },
    ];

    $: currentPath = $page.url.pathname;
    $: pathSegments = currentPath.split('/').filter(Boolean); // Split the path and remove any empty strings
    $: mainPath = '/' + (pathSegments[0] || ''); // Get the main path
    $: subPath = pathSegments[1] || ''; // Get the subpath if any
</script>

<nav>
    <ul class="font-mono">
        {#each links as { href, text }}
            <li>
                <a href={href} class="hover:underline">{href === mainPath ? '* ':''}{text}</a>
                {#if href === mainPath && subPath}
                    <ul>
                        <li><a href={currentPath} class="hover:underline pl-4"> ↳ {subPath}</a></li>
                    </ul>
                {/if}
            </li>
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
