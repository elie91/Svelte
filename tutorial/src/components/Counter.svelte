<script>
  let count = 0;
  //reactive declarations
  // recomputed whenever count change
  $: doubled = count * 2;

  let alert;
  let counter;

  function onClick() {
    count = count + 1;
  }

  $: console.log(`the count is ${count}`);

  $: if (count >= 10) {
    alert.innerText = "The count is too high";
    alert.style.display = "block";
    counter.disabled = true;
  }
</script>

<main>
  <div>
    <p bind:this={alert} class="alert" />
    <button bind:this={counter} on:click={onClick}>Clicked {count} </button>
    <button>Doubled = {doubled} </button>
  </div>
</main>

<style>
  div {
    margin-top: 50px;
  }
  .alert {
    display: none;
    padding: 5px 10px;
    color: white;
    background-color: crimson;
  }
</style>
