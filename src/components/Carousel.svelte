<script>
  // Props
  export let items = [...Array(14).keys()];
  export let scrollBy = 1;

  const paginationFactor = 175;
  const totalPaginationPixels = scrollBy * paginationFactor;

  $: offset = 0;
  $: atStart = offset === 0;
  $: atEnd = offset <= paginationFactor * (items.length - scrollBy) * -1;

  const move = direction => {
    if (direction > 0 && !atEnd) {
      offset -= totalPaginationPixels;
    } else if (direction < 0 && !atStart) {
      offset += totalPaginationPixels;
    }
  };
</script>

<style>
  main {
    width: 100%;
    overflow: hidden;
  }

  .items {
    display: flex;
    transition: transform 0.4s ease-in-out;
    transform: translateX(0px);
  }

  .item {
    min-width: 185px;
    height: 200px;
    margin: 0 4px;
    background-color: #ef4322;
    border-radius: 0.7rem;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: bold;
    font-size: 10rem;
    user-select: none;
    overflow: hidden;
  }

  .items .item:first-child {
    margin-left: 0;
  }

  .items .item:last-child {
    margin-right: 0;
  }

  .layout-button {
    margin-top: 10px;
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
  }

  .button-move {
    border-radius: 50px;
    color: white;
    background-color: #ff3e00;
    width: 50px;
    height: 50px;
    margin-left: 10px;
    cursor: pointer;
  }

  .button-move:hover {
    background-color: #c73404;
  }
</style>

<main>
  <div class="items" style="transform: translateX({offset}px);">
    {#each items as item, i}
      <div class="item" style="background-color: hsla({i * 25}deg, 75%, 55%);">
        {item + 1}
      </div>
    {/each}
  </div>
</main>

<div class="layout-button">
  <button class="button-move" disabled={atStart} on:click={() => move(-1)}>
    &lsaquo;
  </button>
  <button class="button-move" disabled={atEnd} on:click={() => move(1)}>
    &rsaquo;
  </button>
</div>
