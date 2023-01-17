
<script>
    import { page } from '$app/stores';
</script>

<div class="nav-bar">

    <!-- {#each Object.entries(links) as [text, url]}
        <a href={url}>
            <div class="item" class:active={$page.url.pathname === "/" + url}>
                <p>{text}</p>
            </div>
        </a>
    {/each} -->

    <ul>
        <a href="/"><li class:active={$page.url.pathname === "/"}>Home</li></a>
        <a href="/about"><li class:active={$page.url.pathname === "/about"}>About</li></a>
        <a href="/projects"><li class:active={$page.url.pathname === "/projects"}>Projects</li></a>
        <a href="/contact"><li class:active={$page.url.pathname === "/contact"}>Contact</li></a>
    </ul>

    
</div>

<style>
    .nav-bar {
        top: 0;
        position: sticky;
        background-color: none;

        margin: 0;
        padding: 5px;
        /* box-shadow: 0 0.5rem 1rem rgb(0 0 0 / 15%), inset 0 -1px 0 rgb(0 0 0 / 15%) */
    }

    .nav-bar ul {
        margin: 0;
        padding: 0;
    }

    .nav-bar li {
        background-color: none;
        color: var(--main-col-white);

        font-size: large;
        text-align: center;
        
        padding: 10px 10px;
        display: inline-block;
    }

    .nav-bar li:hover {
        background-color: none;
        color: var(--main-col-white);
        outline: 1px solid var(--main-col-accent);

        transition: 0s;
    }

    .nav-bar li.active {
        background-color: var(--main-col-accent);
        color: var(--main-col-black);

        transition: 0.5s;
    }
</style>