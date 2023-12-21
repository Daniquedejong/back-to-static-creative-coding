<script>
	import Electrical from '../lib/components/electrical.svelte';
	import Space from '../lib/components/space.svelte';
</script>

<h1>Creative coding</h1>
<button><a href="/retro">3e creative coding</a></button>
<h2>Insane 90s space psychedelia list</h2>
<br />

<Space />

<br />
<h2>Electrical experimental escapist carousel</h2>
<br />

<Electrical />

<style>
	button {
		border: none;
		padding: 1em;
		margin: 1em;
		margin-left: 50em;
		border-radius: 10px;
		box-shadow: lightgrey 1px 1px 10px 1px;
		font-weight: 600;

        --h: 30;
        --s: 70%;
        --l: 50%;
        --a: 1;
        background: hsl(var(--h) var(--s) var(--l)/var(--a));
	}

	button:hover {
	    --l: 65%;
	}

    button:focus {
        --s: 25%;
    }

	a {
		text-decoration: none;
	}
</style>
