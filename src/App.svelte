<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'

  let color = "black"
  const handleClick = () => {
    color = "orange"
  }
  // const handleInput = (e) => {
  //   color = e.target.value
  // }
</script>

<main>
  <h1 style="color: {color}">{color}</h1>

<button on:click={handleClick}>update color</button>

<!-- <input type="text" on:input={handleInput}  value={color}> -->
<input type="text" bind:value={color}> <!--shorthand for the input field above -->
</main>

<style >

</style>
