<script>
    import Header from '../../components/Header.svelte';
    import StyleLink from '../../components/StyleLink.svelte';
    import LastFM from "../../components/LastFM.svelte";
</script>

<Header />

<div class="m-4 font-mono sm:flex md:flex lg:flex justify-between">
    <div class="m-4">
        <h1 class="text-xl">hardware</h1>
        <ul class="text-sm list-disc p-2">
            <li>Macbook Pro (M2 Pro, 16GB RAM, 512GB SSD)</li>
            <li>AKG K371</li>
            <li>Ducky One 2 (Cherry MX silent red)</li>
            <li>Logitech G502 Mouse</li>
            <li>Raspberry Pi 3b+</li>
            <li>Airpods Pro</li>
        </ul>

        <br>

        <h1 class="text-xl">software</h1>
        <ul class="text-sm list-disc p-2">
            <li>neovim (<StyleLink url="https://github.com/arnavsurve/nvim">my config</StyleLink>)</li>
            <li>obsidian.md</li>
            <li>zsh + oh-my-zsh</li>
            <li>tmux</li>
        </ul>

        <br>

    </div>

    <br>

    <div class="font-mono min-w-fit mx-2">
        <h1 class="text-xl mb-2">my top 10 weekly (<StyleLink url="https://www.last.fm/user/arnavsurve">last.fm</StyleLink>)</h1>
        <LastFM />
    </div>
</div>