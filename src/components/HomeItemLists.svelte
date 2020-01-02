<script>
  import CardItem from "./CardItem.svelte";
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
  <CardItem />
  <CardItem />
  <CardItem />
  <CardItem />
  <CardItem />
  <CardItem />
</div>
