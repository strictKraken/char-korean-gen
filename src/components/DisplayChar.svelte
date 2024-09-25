<script lang="ts">
	let { char }: { char: string } = $props();
</script>

<div class="char-wrapper">
	<span class="char">
		{char}
	</span>
</div>

<style>
  .char-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
  }
	.char {
		font-size: 20em;
	}
</style>
