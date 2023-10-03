<h1>Welcome!</h1>

<canvas bind:this={canvas} ></canvas>

<script>
	import {onMount} from 'svelte';

	let canvas;

	onMount(()=>
		{
			const ctx = canvas.getContext('2d');
			let frame = requestAnimationFrame(loop);

			function loop(t){
				frame = requestAnimationFrame(loop);
				ctx.fillRect(10,10, 20, 20);
			};
		})
</script>


<style>
	canvas {
		width: 100%;
		height: 100%;
	}
</style>