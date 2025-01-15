<script lang="ts">
    type PointerEvent = {
        x: number
        y: number
    }

	let m = $state({ x: 0, y: 0 });

	function onMove(event: PointerEvent) {
		m.x = event.x;
		m.y = event.y;
	}
</script>

<div onpointermove={onMove}>
	The pointer is at {Math.round(m.x)} x {Math.round(m.y)}
</div>

<style>
	div {
		width: 500px;
		height: 200px;
		padding: 1rem;
        border: 1px solid #ccc;
	}
</style>
