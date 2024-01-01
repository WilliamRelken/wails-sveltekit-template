<script lang="ts">
  import { Greet } from "$lib/wailsjs/go/main/App";

  let name: string;
  async function greet() {
    alert(await Greet(name));
  }
</script>

<form>
  <input type="text" bind:value={name} />
  <button on:click={greet}>Greet</button>
</form>
