<script>
import Electrical from "../lib/components/electrical.svelte";
	import Retro from "../lib/components/retro.svelte";
import Space from "../lib/components/space.svelte";

</script>

<h1>Creative coding</h1><button><a href="src/routes/retro.svelte">3e creative coding</a></button>
<h2>Insane 90s space psychedelia list</h2><br>

<Space />

<br><h2>Electrical experimental escapist carousel</h2><br>

<Electrical />

<Retro />

<style>
    button {
        background-color: lightpink;
        color: black;
        border: none;
        padding: 1em;
        margin: 1em;
        margin-left: 50em;
        border-radius: 10px;
        box-shadow: lightgrey 1px 1px 10px 1px;
        font-weight: 600;
    }

    button:hover {
        background-color: black;
        color: lightpink;
    }

    a {
        text-decoration: none;
    }
</style>