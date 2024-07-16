<script>
    import Header from '../../components/Header.svelte';
    import Prose from '../../components/Prose.svelte';
    import StyleLink from '../../components/StyleLink.svelte';
</script>

<Header />

<div class="m-4 font-mono">
    <StyleLink classDefs="text-lg" url="https://github.com/arnavsurve/website">
        this website - july 2024
    </StyleLink>

    <Prose>
        This is my personal portfolio built using SvelteKit for the frontend UI and TailwindCSS for styling components. The source code is available on GitHub at the link above, and I am using Vercel for deployment and hosting. The design of this website is inspired by the <StyleLink url={"https://tinygrad.org/"}>tinygrad</StyleLink> website.
    </Prose>

</div>