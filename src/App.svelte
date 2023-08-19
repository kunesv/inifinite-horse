<script>
	import { onMount } from "svelte";

	onMount(() => {
		const NOHY = document.querySelector(".Nohy");
		var delkaNohou = 0;
		let cloneNohy = () => {
			document.querySelector(".Kun").append(NOHY.cloneNode(true));
		};
		window.onscroll = () => {
			if (delkaNohou < 1000) {
				cloneNohy();
				delkaNohou++;
			} else {
				document.querySelector(".Link").classList.remove("hidden");
			}
		};
		for (let i = 0; i < 100; i++) {
			cloneNohy();
		}
		window.scrollTo({ top: 0, left: 0 });
	});
</script>

<main>
	<div class="Kun">
		<pre>
            O
       ()      -----------
            ||         ||
            ||         ||</pre>
		<pre class="Nohy">            ||         ||</pre>
	</div>
	<div class="Link hidden">
		<pre class="Nohy">            ||         ||</pre>
		<pre class="Nohy">          ----       ----</pre>
		<p><a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Click Here!</a></p>
	</div>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
	pre {
		margin: 0;
	}
	.hidden {
		display: none;
	}
	.Link p {
		margin-top: 2rem;
	}
</style>
