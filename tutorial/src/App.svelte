<script>
  export let name;
  import Image from "./components/Image.svelte";
  import Counter from "./components/Counter.svelte";
  import Sum from "./components/Sum.svelte";
  import List from "./components/List.svelte";
  import AsyncPost from "./components/AsyncPost.svelte";
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
  <Image
    src="https://images.unsplash.com/photo-1627215477561-f0b7755115e9?ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=60"
    alt="paysage"
  />
  <Counter />
  <Sum />
  <List />
  <AsyncPost postId={1} />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: 1200px;
    }
  }
</style>
