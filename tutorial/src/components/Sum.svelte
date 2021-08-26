<script>
  let numbers = [];
  let value = "";

  function onChange(event) {
    value = event.target.value;
  }

  function onClick() {
    if (value.length === 0) return;
    numbers = [...numbers, +value];
    value = "";
  }

  $: sum = numbers.reduce((acc, value) => acc + value, 0);
</script>

<main>
  {#if numbers.length}
    <p>{numbers.join(" + ")} = {sum}</p>
  {/if}
  <div class="flex">
    <input
      on:change={onChange}
      type="number"
      placeholder="Saisir un chiffre"
      {value}
    />
    <button on:click={onClick}>Valider</button>
  </div>
</main>

<style>
  main {
    margin-top: 50px;
  }
  .flex {
    display: flex;
    justify-content: center;
  }
</style>
