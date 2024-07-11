<script>
    import { onMount } from "svelte";
    import Navbar from "./Navbar.svelte";

    onMount(() => {
        const name = document.getElementById("name");
        const text = "arnav surve";
        let i = 0;
        const type = () => {
            if (i < text.length) {
                // @ts-ignore
                name.innerHTML += text.charAt(i);
                i++;
                setTimeout(type, 70);
            }
        };
        type();
    });
</script>

<div class="flex items-center justify-between font-mono p-4">
    <h1 id="name" class="text-slate-500 text-3xl">
    </h1>

    <div class="justify-end">
        <a href="mailto:arnavsurve@gmail.com">arnavsurve@gmail.com</a>
        <a href="https://www.github.com/arnavsurve">github</a>
        <a href="https://www.linkedin.com/in/arnavsurve/">linkedin</a>
        <!-- <a href="https://leetcode.com/u/arnavsurve/">leetcode</a> -->
    </div>
</div>

<Navbar />
