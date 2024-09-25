<script lang="ts">
	import DisplayChar from './DisplayChar.svelte';

	let { onClickAction, char }: { onClickAction: () => void, char: string } = $props();
</script>

<section>
	<div>
		<div>
			<DisplayChar char={char} />
		</div>
		<div>
			<button class="button" onclick={() => onClickAction()}>next</button>
		</div>
	</div>
</section>

<style>
  .button {
    width: 100%;
    font-size: 2em;
  }
</style>
