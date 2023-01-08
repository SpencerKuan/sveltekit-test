<script>
	import { each } from "svelte/internal";

    export const links = {
        about: "hi",
        contact: "contact",
        projects: "projects"
    };
</script>

<div>
    <h1>links go here:</h1>

    {#each Object.entries(links) as [text, url]}
        <p>{text}</p>
    {/each}
</div>