<script defer src="https://pyscript.net/alpha/pyscript.js">
    import Header from "../../../components/Header.svelte";
    import Prose from "../../../components/Prose.svelte";
    import StyleLink from "../../../components/StyleLink.svelte";
    // import Codeblock from "../../../components/Codeblock.svelte";

    // import Prism from 'svelte-prism';
    // import 'prismjs/themes/prism-tomorrow.css';
</script>

<Header />

<div class="m-4 font-mono">
    <h1 class="text-xl mb-1">last.fm-crawl</h1>
    <Prose classDefs="p-2 mb-4">
        HTML embed solutions for Last.fm stats suck! They are either not customizable, slow, or most of the time both. I wanted to create a simple, fast, and customizable solution for embedding Last.fm stats on my website. This is an overview on how I created my own Flask API to fetch Last.fm stats and deployed it on AWS Lambda. By placing responsibility the on the end user <b>(myself and whoever else I trust to not blow up my AWS bills)</b> for handling the frontend and styling, I was able to create a fast and customizable solution for embedding LastFM stats with maximum granularity and reproducibility across multiple website themes and Last.fm users with the power of JSON.
    </Prose>

    <h2 class="text-md mb-1">python last.fm library</h2>
    <Prose classDefs="p-2 mb-4">
        To interact with the Last.fm API, I used the <StyleLink url="https://github.com/pylast/pylast">pylast</StyleLink> library, a Python wrapper for the Last.fm API. I chose this as it is simple to get up and running and gives access to all the data exposed by the Last.fm web interface. The library also provides access to other data such as top artists, top albums, and more. To handle my Last.fm API credentials, I used environment variables to store my API key, API secret, username, and password in a file named `config.json`.
    </Prose>

    <!-- <Prism language="html" source="print('hello')"></Prism> -->
    <!-- <script src="https://gist.github.com/arnavsurve/31a932cf4f0f352d0ca2d1185182c3fd.js"></script> -->

</div>
