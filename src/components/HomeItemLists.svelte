<script>
  import CardItem from "./CardItem.svelte";

  export let items = [];
</script>

<style>
  .home-list-container {
    display: block;
    background-color: #ff3e00;
    padding: 40px 20px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
</style>

<div class="home-list-container">
  {#each items as item}
    <CardItem title={item.title} />
  {:else}
    <p>Loading...</p>
  {/each}
</div>
