<script>
    export let url = "#";
    export let classDefs= "";
</script>

<div class={"inline " + classDefs}>
    <a class="text-slate-500 hover:underline font-mono" href={url}>
        <slot></slot>
    </a>
</div>