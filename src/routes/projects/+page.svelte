<script>
    import Header from '../../components/Header.svelte';
    import Prose from '../../components/Prose.svelte';
    import StyleLink from '../../components/StyleLink.svelte';
</script>

<Header />

<div class="m-4 font-mono">
    <StyleLink classDefs="text-xl" url="/projects/lastfm-crawl">
        last.fm-crawl - july 2024
    </StyleLink>

    <Prose classDefs="p-2">
        Wondering how I display my recent listens in <StyleLink url="/misc">/misc</StyleLink>? This blog post walks through my process building a Flask API that fetches my top weekly and recent tracks from <StyleLink url="https://www.last.fm/home">last.fm</StyleLink> and returns them as JSON. The API is hosted on AWS Lambda and a blog post walking through my implementation is linked above. Code hosted on <StyleLink url="https://github.com/arnavsurve/lastfm-crawl">GitHub</StyleLink>.
    </Prose>

    <br>

    <div>
        <StyleLink classDefs="text-xl" url="https://github.com/arnavsurve/website">
            this website - july 2024
        </StyleLink>
        <Prose classDefs="p-2">
            This is my personal portfolio built using SvelteKit for the frontend UI and TailwindCSS for styling components. The source code is available on GitHub at the link above, and I am using Vercel for deployment and hosting. The design of this website is inspired by the <StyleLink url={"https://tinygrad.org/"}>tinygrad</StyleLink> website.
        </Prose>
    </div>
</div>
