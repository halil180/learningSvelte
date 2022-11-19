<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'

$:fullname= `${firstName} ${lastName}` /// reactive value

  let color = "black"
  const handleClick = () => {
    color = "orange"
  }

  $:{
    console.log(firstName)
    console.log(color)
  }

  // const handleInput = (e) => {
  //   color = e.target.value
  // }
  let firstName = "jimi"
  let lastName = "hendrix"
</script>

<main>
  <h1 style="color: {color}">{color}</h1>
  <p>{fullname}</p>
<button on:click={handleClick}>update color</button>

<!-- <input type="text" on:input={handleInput}  value={color}> -->

<input type="text" bind:value={color}> <!--shorthand for the input field above -->
<input type="text" bind:value={firstName}>
<input type="text" bind:value={lastName}>
</main>

<style >

</style>
