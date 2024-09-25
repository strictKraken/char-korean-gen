<script lang="ts">
	import CardChar from "../components/CardChar.svelte";
  import { KOREAN_CHARS } from "$lib/korean-chars";

  const getRandomValueFromArray = <T>(array: T[]): T => {
    return array[Math.floor(array.length * Math.random())];
  }

  let currentChar = $state(getRandomValueFromArray<string>(KOREAN_CHARS));

  const genNextChar = () => {
    currentChar = getRandomValueFromArray(KOREAN_CHARS);
  }
</script>
<main>

  <CardChar char={currentChar} onClickAction={() => genNextChar()}/>
</main>