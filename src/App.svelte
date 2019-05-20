<script>
  import CustomInput from "./CustomInput.svelte";
  import Toggle from "./Toggle.svelte";

  let value = "";
  let chosenOption;
  let price;
  $: console.log(value);
</script>

<CustomInput bind:val={value} />
<Toggle bind:chosenOption />
<div> {chosenOption} </div>

<input type="number" value={price} bind:value />
