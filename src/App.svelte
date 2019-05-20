<script>
  import CustomInput from "./CustomInput.svelte";
  import Toggle from "./Toggle.svelte";

  let value = "";
  let chosenOption;
  let price;
  let agreed;
  $: console.log(value);
  $: console.log(agreed);
</script>

<CustomInput bind:val={value} />
<Toggle bind:chosenOption />
<div> {chosenOption} </div>

<input type="number" value={price} bind:value />

<label>
  <input type="checkbox" bind:checked={agreed} />
  Aree to terms?
</label>
