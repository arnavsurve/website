<script lang="ts">
    import Prism from 'svelte-prism';
    import 'prismjs/themes/prism-tomorrow.css';

    let inlineCode = "";
    let lang=""
</script>

<Prism language="{lang}" source={inlineCode}></Prism>