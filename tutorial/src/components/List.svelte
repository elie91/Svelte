<script>
  let cats = [
    { id: "J---aiyznGQ", name: "Keyboard Cat" },
    { id: "z_AbfPXTKms", name: "Maru" },
    { id: "OUtn3pvWmpg", name: "Henri The Existential Cat" },
  ];
</script>

<div>
  <h1>The Famous Cats of YouTube</h1>

  <ul>
    <!-- loop args: value, index, key -->
    {#each cats as cat, i (cat.id)}
      <li>
        <a target="_blank" href="https://www.youtube.com/watch?v={cat.id}">
          {cat.name}
        </a>
      </li>
    {/each}
  </ul>
</div>

<style>
  div {
    max-width: 40%;
    margin: 50px auto;
  }
</style>
