<script>
  export let title = "title card";
  export let img;
  export let details =
    "Quis cillum aute mollit sunt voluptate. Veniam commodo reprehenderit magna eu nisi pariatur et aliquip dolore commodo deserunt ad sit.";
  export let price = "Rp. ";
</script>

<style>
  .card {
    width: 220px;
    height: 320px;
    border-radius: 10px;
    /* box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.07); */
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    text-align: left;
    margin-bottom: 10px;
    background-color: white;
  }

  .bg-image {
    background-color: darkgrey;
    width: 100%;
    height: 45%;
    border-radius: 10px 10px 0px 0px;
  }

  .content-card {
    padding: 2px 16px;
  }

  .title {
    font-size: 20px;
    padding: 10px 0px;
    font-weight: 600;
    text-transform: capitalize;
    font-weight: 700;
  }

  .details {
    width: 100%;
    height: 200px;
    font-size: 14px;
  }
</style>

<div class="card">
  {#if img == null}
    <div class="bg-image" />
  {:else}
    <img src={img} alt="" />
  {/if}
  <div class="content-card">
    <div class="title">{title}</div>
    {#if details != null}
      <div class="details">{details}</div>
    {/if}
    {#if price != null}
      <div class="price">{price}</div>
    {/if}
  </div>
</div>
