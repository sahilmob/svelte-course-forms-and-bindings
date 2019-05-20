<script>
  import CustomInput from "./CustomInput.svelte";
  import Toggle from "./Toggle.svelte";

  let value = "";
  let chosenOption;
  let price;
  let agreed;
  let favColor = "green";
  let favColorCheck = ["green"];
  let favColorSelect = "green";
  let usernameInput;
  let customInput;

  $: console.log(value);
  $: console.log(agreed);
  $: console.log(favColor);
  $: console.log(favColorCheck);
  $: console.log(favColorSelect);
  $: console.log(customInput);

  function saveData() {
    console.log(usernameInput.value);
    customInput.empty();
  }
</script>

<CustomInput bind:val={value} bind:this={customInput} />
<Toggle bind:chosenOption />
<div> {chosenOption} </div>

<input type="number" value={price} bind:value />

<label>
  <input type="checkbox" bind:checked={agreed} />
  Aree to terms?
</label>

<label>
  <input type="radio" name="color" value="red" bind:group={favColor} />
  Red
</label>

<label>
  <input type="radio" name="color" value="green" bind:group={favColor} />
  Green
</label>
<label>
  <input type="radio" name="color" value="blue" bind:group={favColor} />
  Blue
</label>

<label>
  <input type="checkbox" name="color" value="red" bind:group={favColorCheck} />
  Red
</label>

<label>
  <input
    type="checkbox"
    name="color"
    value="green"
    bind:group={favColorCheck} />
  Green
</label>
<label>
  <input type="checkbox" name="color" value="blue" bind:group={favColorCheck} />
  Blue
</label>

<select bind:value={favColorSelect}>
  <option value="green">green</option>
  <option value="blue">blue</option>
  <option value="red">red</option>
</select>

<input type="text" bind:this={usernameInput} />
<button on:click={saveData}>Save</button>
