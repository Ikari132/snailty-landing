<script lang="ts">
	export let id: string;
</script>

<a class="anchor" {id} />

<style lang="scss">
	a.anchor {
		display: block;
		position: relative;
		top: -(76px + 24px);
		visibility: hidden;
	}
</style>
