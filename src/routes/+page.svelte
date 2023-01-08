<script>
    var name = "bob";
    var age = 2;

    let number = 2;

    function add(){
        number = number + 1;
        console.log(window);
    }

    import Nav from "./Nav.svelte";
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<Nav></Nav>

<h2>My name is {name}</h2>
<p>I am {age} years old</p>


<button on:click={add}>Clicked {number} times</button>
<ul>
    {#each Array(number).fill(0).map((x, i) => i) as i}
        <li>Item {i}</li>
    {/each}
</ul>
