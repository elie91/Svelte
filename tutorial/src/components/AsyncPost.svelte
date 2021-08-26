<script>
  export let postId;
  async function getPost() {
    const res = await fetch(
      `https://jsonplaceholder.typicode.com/posts/${postId}`
    );
    const post = await res.json();
    if (res.ok) {
      return post;
    } else {
      throw new Error("Error while fetching post");
    }
  }

  let promise = getPost();
</script>

<div>
  {#await promise}
    <p>...waiting</p>
  {:then post}
    <h1>Titre du post {post.id}</h1>
    <p>{post.title}</p>
  {:catch error}
    <p>error</p>
  {/await}
</div>
