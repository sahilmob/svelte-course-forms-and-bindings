<script>
  import CustomInput from "./CustomInput.svelte";
  import Toggle from "./Toggle.svelte";

  let value = "";
  let chosenOption;
  $: console.log(value);
</script>

<CustomInput bind:val={value} />
<Toggle bind:chosenOption />
<div> {chosenOption} </div>
