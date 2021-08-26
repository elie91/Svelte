<script>
  export let src;
  export let alt;
</script>

<main>
  <img {src} {alt} />
</main>

<style>
  img {
    border-radius: 10px;
    width: 300px;
    height: auto;
  }
</style>
