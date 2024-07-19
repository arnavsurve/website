<script>
    import Header from '../../components/Header.svelte';
    import StyleLink from '../../components/StyleLink.svelte';
    import LastFM_top from "../../components/LastFM_top.svelte";
    import LastFM_recent from "../../components/LastFM_recent.svelte";
</script>

<Header />

<div class="font-mono sm:flex md:flex lg:flex justify-between">
    <div class="mx-4">
        <h1 class="text-xl">hardware</h1>
        <ul class="text-sm list-disc p-2">
            <li>Macbook Pro (M2 Pro, 16GB RAM, 512GB SSD)</li>
            <li>AKG K371</li>
            <li>Airpods Pro</li>
            <li>Ducky One 2 (Cherry MX silent red)</li>
            <li>Logitech G502</li>
            <li>Raspberry Pi 3b+</li>
        </ul>

        <br>

        <h1 class="text-xl">software</h1>
        <ul class="text-sm list-disc p-2">
            <li>neovim (<StyleLink url="https://github.com/arnavsurve/nvim">my config</StyleLink>)</li>
            <li>obsidian.md</li>
            <li>zsh + oh-my-zsh</li>
            <li>tmux</li>
        </ul>
    </div>

    <br>

    <div class="font-mono min-w-fit mx-4">
        <h1 class="text-xl mb-2">recent listens (<StyleLink url="https://www.last.fm/user/arnavsurve">last.fm</StyleLink>)</h1>
        <LastFM_recent />
    </div>
</div>
