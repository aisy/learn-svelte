<script>
  import Button from "./ButtonComponent.svelte";
</script>

<style>
  header {
    width: 100%;
    padding: 6px 25px;
    position: fixed;
    top: 0;
    background-color: transparent;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.07);
  }

  logo {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 1.5em;
    font-weight: 700;
  }

  .right-menu {
    float: right;
  }

  .right-menu li {
    float: left;
    color: #ff3e00;
    text-align: center;
    text-transform: uppercase;
    font-size: 14px;
    list-style: none;
    font-weight: 700;
    padding: 8px 20px 0px 0px;
  }
</style>

<header>
  <logo>LaLiLuLeLo</logo>
  <div class="right-menu">
    <li>menu1</li>
    <li>menu2</li>
    <li>menu3</li>
    <li>menu4</li>
    <!-- <button class="button-menu">klik me</button> -->
    <Button title="Masuk" />
  </div>
</header>
