<script>
    import Header from '../../components/Header.svelte';
    import Prose from '../../components/Prose.svelte';
    import StyleLink from '../../components/StyleLink.svelte';
</script>

<Header />

<div class="m-4 font-mono">
    <!-- <StyleLink classDefs="text-xl" url="/projects/lastfm-crawl"> -->
    <StyleLink classDefs="text-xl" url="https://github.com/arnavsurve/lastfm-crawl">
        last.fm-crawl - july 2024
    </StyleLink>

    <Prose classDefs="p-2">
        HTML embed solutions for Last.fm stats suck - they are either not customizable, slow, or most of the time both. I wanted to create a performant, customizable, and versatile solution for embedding Last.fm stats on my website at <StyleLink url="/misc">/misc</StyleLink>. This is a wrapper for the <StyleLink url="https://www.last.fm/home">last.fm</StyleLink> API written in Python (Flask), containerized with Docker, and hosted with AWS Lambda for personal use. The goal was to provide endpoints that only returned JSON, allowing the developer to display data in the frontend as they wish. Code hosted on GitHub at the link above.
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
