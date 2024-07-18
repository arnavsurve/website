<script>
    export let classDefs = "";
</script>


<div class={"max-w-full md:max-w-[80%] lg:max-w-[70%] " + classDefs}>
    <p class="font-mono text-sm">
        <slot></slot>
    </p>
</div>
