<script>
  export let username;

  import { Collection } from "sveltefire";
  import Firebase from "../../components/Firebase.svelte";
</script>

<Firebase>
  <Collection
    path={'users'}
    query={(ref) => ref.where('username', '==', username)}
    let:data={curUser}>
    <div slot="fallback">error</div>
    <div slot="loading">loading</div>
    <h2>Hello {curUser[0].firstname}</h2>
  </Collection>
</Firebase>
