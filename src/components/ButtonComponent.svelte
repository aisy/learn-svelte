<script>
  export let title = "Button";
  export let buttonWidth = 90;
</script>

<style>
  .button-menu {
    border-radius: 30px;
    background-color: #ff3e00;
    color: #fff;
    margin: 0px;
    width: var(--buttonWidth) px;
    padding: 10px;
  }

  .button-menu:hover {
    background-color: #fff;
    color: #ff3e00;
    border-color: #ff3e00;
    cursor: pointer;
  }
</style>

<button class="button-menu">{title}</button>
