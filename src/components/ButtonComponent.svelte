<script>
  export let color = "#ff3e00";
  export let title = "Button";
</script>

<style>
  .button-menu {
    border-radius: 20px;
    /* background-color: #{$color}; */
    color: #fff;
    width: 90px;
    margin: 0px;
  }

  .button-menu:hover {
    background-color: #fff;
    color: #ff3e00;
    border-color: #ff3e00;
    cursor: pointer;
  }
</style>

<button class="button-menu" style="background-color:{color}">{title}</button>
